<template>
  <view class="stores">
    <view class='page'></view>
    <view class='page_content'>
    <view class="index-swiper">
      <swiper indicator-dots autoplay interval="5000" duration="1000">
        <block>
          <swiper-item>
            <image  src="https://www.trksyy.com/uploads/20230114/c0f3e7affa7f6e1a725e828a98695c61.png?696753127705959" class="swiper-image" />
          </swiper-item>
        </block>
      </swiper>
      </view>
      <view class='func-area'>
        <navagator class='func_item' v-for="(item,index) in 10" :key="index">
          <image src="../../static/images/icon_carticon.png"></image>
          <text>餐饮美餐</text>
        </navagator>
      </view>

      <view class='store_cart'>
         <view class="goods_title_box">
          <view class="goods_title">-店铺推荐-</view>
          </view>
            <!-- 导航 -->
          <view class="sticky-box">
            <!-- 滑动区域 -->
            <scroll-view class="scroll-view_H"  scroll-x="true" scroll-with-animation :scroll-left="tabsScrollLeft" @scroll="scroll">
              <view class="tab" id="tab_list">
                <view id="tab_item" :class="{ 'active': listActive == index,'tab__item':true}" v-for="(item, index) in listArr" :key="index" @click="clickSort(index)">
                  {{item.title}}
                </view>
              </view>
              <!-- tabs下划线 -->
              <view class="tab__line"
                  :style="{background: lineColor, width: lineStyle.width, transform: lineStyle.transform,transitionDuration: lineStyle.transitionDuration}">
              </view>
            </scroll-view>
        
          </view>
          <!-- 列表 -->
          <view class="carts-item" v-for="(item,index) in 10" :key="index">
            <view>
              <image src="https://swjls.shuxiaoliu.com//Uploads/image/goods/2022-08-10/62f3436390580.jpg" class="carts-image" mode="scaleToFill"></image>
            </view>
            <view class="carts-text">
              <view class="carts-title"  >
                <text>饮美食餐饮美食美食食</text>
              </view> 
              <view class="carts-status">
                <view   class="shop_status">122km</view>
              </view>
              <view class="goods-score" >
                <view>福建省宁德时代</view>
              </view>
            </view>
          </view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: "stores",
  components: {},
  props: {},
  data() {
    return {
    listArr: [{title:"最近"},{title:"推荐"},{title:"人气"}],
		listActive: 0,   // 当前选中项
		tabsScrollLeft: 0,  // tabs当前偏移量
		scrollLeft:0,
		lineStyle: {},    // 下划线位置--动态甲酸
		duration: 0.2    // 下划线动画时长

    }
  },
  computed: {},
  methods: {
    clickSort (index) {
		this.listActive = index
	},
	// scroll-view滑动事件
	scroll(e) {
		this.scrollLeft = e.detail.scrollLeft;
	},
	setTabList() {
		this.$nextTick(()=>{
			this.setLine()
			this.scrollIntoView()
		})
	},
	// 计算tabs位置
	scrollIntoView() {  // item滚动
		let lineLeft = 0;
		this.getElementData('#tab_list', (data)=> {
			let list = data[0]
			this.getElementData(`#tab_item`, (data)=> {
				let el = data[this.listActive]
				lineLeft = el.width / 2 + (-list.left) + el.left - list.width / 2 - this.scrollLeft
				this.tabsScrollLeft = this.scrollLeft + lineLeft
			})
		})
	},
	//  计算下划线位置
	setLine() {
		let lineWidth = 0, lineLeft = 0
		this.getElementData(`#tab_item`, (data)=> {
			let el = data[this.listActive]
			lineWidth = el.width / 2
			// lineLeft = el.width * (this.currentIndex + 0.5)  // 此种只能针对每个item长度一致的
			lineLeft = el.width / 2 + (-data[0].left) + el.left
			this.lineStyle = {
				width: `${lineWidth}px`,
				transform: `translateX(${lineLeft}px) translateX(-50%)`,
				transitionDuration: `${this.duration}s`
			};
		})
	},
	getElementData(el, callback){
		uni.createSelectorQuery().in(this).selectAll(el).boundingClientRect().exec((data) => {
			callback(data[0]);
		});
	},


  },
  watch: {
    listActive(newVal) {     // 监听当前选中项
  		this.setTabList()
  	}
  },

  // 页面周期函数--监听页面加载
  onLoad() {
    
  },
 
  // 页面周期函数--监听页面初次渲染完成
  onReady() {
    this.setTabList()

  },
  // 页面周期函数--监听页面显示(not-nvue)
  onShow() {

  },
  // 页面周期函数--监听页面隐藏
  onHide() {},
  // 页面周期函数--监听页面卸载
  onUnload() {},
  // 页面处理函数--监听用户下拉动作
  // onPullDownRefresh() { uni.stopPullDownRefresh(); },
  // 页面处理函数--监听用户上拉触底
  // onReachBottom() {},
  // 页面处理函数--监听页面滚动(not-nvue)
  // onPageScroll(event) {},
  // 页面处理函数--用户点击右上角分享
  // onShareAppMessage(options) {},
} 
</script>

<style lang="scss" scoped>
.page{ 
  position: fixed;
  background-color: #f3f3f3;
  height: 100%;
  width: 100%;
  top: 0;
  z-index: -1;
 
}

.index-swiper{
  padding: 10rpx 28rpx;
} 
.swiper-image {
  width: 100%;
  height: 300rpx;
}
.func-area {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  padding: 18rpx 0rpx;
  background: white;
  margin: 10rpx 28rpx;
  border-radius: 16rpx;
}
.func-area  .func_item{
  width: 20%;
  text-align: center;
  margin-top: 20rpx;
}
.func-area image {
  width: 110rpx;
  height: 110rpx;
}
.func-area text {
  display: block;
  color: #6c6c6c;
  font-size: 0.8rem;
  line-height: 50rpx;
}
.goods_title_box{
  background-color: #fff;
  display: flex;
  justify-content: center;
  padding: 28rpx;

}
.goods_title {
  height: 60rpx;
  width: 238rpx;
  text-align: center;
  background-repeat: no-repeat;
  font-weight: bold;
  background-position: center center;
  display: flex;
  justify-content: center;
  text-align: center;
}
.sticky-box {
  /* #ifndef APP-PLUS-NVUE */
  display: flex;
  position: -webkit-sticky;
  /* #endif */
  position: sticky;
  top: var(--window-top);
  z-index: 99;
  flex-direction: row;
  margin: 0px;
  border-top: 1px #f9f9f9 solid;
  border-bottom: 1px #f9f9f9 solid;
  background: #fff;
}
.tab {
  position: relative;
  display: flex;
  font-size: 28rpx;
  padding-bottom: 10rpx;
  white-space: nowrap;
  &__item {
    flex: 1;
    padding: 0 20rpx;
    text-align: center;
    height: 60rpx;
    line-height: 60rpx;
    color: #666;
    &.active {
      color: #f9ae3d;
    }
  }
}
.tab__line {
  display: block;
  height:6rpx;
  position: absolute;
  bottom: 0;
  left: 0;
  z-index: 1;
  border-radius: 3rpx;
  position: relative;
  background: #f9ae3d;
}
.scroll-view_H {
  /* 文本不会换行，文本会在在同一行上继续，直到遇到 <br> 标签为止。 */
  white-space: nowrap;
  width: 100%;
}

.scroll-view_H{
  white-space:nowrap;
  width: 100%;
box-sizing: border-box;
} 
.carts-item {
  display: flex;
  flex-direction: row;
  height: 20%;
  padding: 30rpx;
  /* border-radius: 20rpx; */
  background-color: #ffffff;
  margin:10rpx 25rpx;
  border-bottom: 1rpx solid #f7f7f7;
}
.carts-image {
  width:180rpx;
  height:180rpx;
}
.carts-text {
  margin-left: 20rpx;
  width: 750rpx;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.carts-title {
  font-size: 0.89rem;
  height:80rpx;
  line-height:40rpx;
  display: -webkit-box;
  overflow: hidden;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 2;
}

.carts-status{
  position: relative;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.carts-status .shop_status{
  color: #aaaaaa;
  font-size:12px;
  line-height: 22px;
  padding: 0px 10px;
 
  border-radius: 2px;
  border: 1rpx solid #f8f8f8;
}
.carts-status .shop_status.on{
  background-color: #5582e4;
}
.goods-score {
  display: flex;
  flex-direction: row;
  justify-content: left;
  width: 100%;
  font-size: 24rpx;
  color:rgb(216, 216, 216);

}
.index-swiper{
  padding: 10rpx 36rpx;
}
.index-swiper image{
  border-radius: 20rpx;
}

</style>