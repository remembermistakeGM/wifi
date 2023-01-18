<template>
  <view class="storeDetail">
    <view class='page'></view>
    <view class='store_info'>
      <view class='store_info_left'>
        <view class='store_img'><image mode="scaleToFill" src="https://swjls.shuxiaoliu.com//Uploads/image/goods/2022-10-27/6359f2ee608fa.png"></image></view>
          <view class='store_textbox'>
            <view class='store_name'>汽修</view>
            <view class='store_text'>简介</view>  
            <view class='store_text'>151145545545</view>  
            <view class='store_text'>附件省安顺市</view>  
          </view>
      </view>
    </view>

    <view class="head-icon-item">
      <view class="head-icon">
      <image src="/static/icons/wifi.svg"></image>
      <text>一键快速连接</text>
      </view>
      <view class="head-icon">
      <image src="/static/icons/lock-closed-outline.svg"></image>
      <text>无需告知密码</text>
      </view>
      <view class="head-icon">
      <image src="/static/icons/planet.svg"></image>
      <text>安全防蹭网</text>
      </view>
      </view>
      <view class='store_info1'> 
        <view class='connect_image'><image src="/static/icons/wifi-orange.svg"></image></view>
        <view class='connect_btn'><button>一键安全连接WiFi</button></view>
        <view class='connect_text'>连接前请打开手机WiFi及定位功能</view>
      </view>

       <view class=''>
        <view class='carts-item-title'>附近上架</view>
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
          <view class="goods-score">
            <view>福建省宁德时代</view>
          </view>
        </view>
      </view>
    </view> 

  </view>
</template>

<script>
export default {
  name: "storeDetail",
  components: {},
  props: {},
  data() {
    return {}
  },
  computed: {},
  methods: {},
  watch: {},

  // 页面周期函数--监听页面加载
  onLoad() {},
  // 页面周期函数--监听页面初次渲染完成
  onReady() {},
  // 页面周期函数--监听页面显示(not-nvue)
  onShow() {},
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

<style scoped>

.page{ 
  position: fixed;
  background-color: #f3f3f3;
  height: 100%;
  width: 100%;
  top: 0;
  z-index: -1;
 
}
.store_info{
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 18rpx 0rpx;
  background: white;
  margin: 10rpx 28rpx;
  border-radius: 16rpx;
}
.store_info1{

  padding: 18rpx 0rpx;
  background: white;
  margin: 10rpx 28rpx;
  border-radius: 16rpx;
}
.store_info_left{
    display: flex;
   flex-direction: row;
}
.store_img image{
  width: 180rpx;
  height: 180rpx; 
  margin: 20rpx; 
}
.store_textbox{
  margin-top: 20rpx;
}
.store_name{
  font-weight: bold;
}
.store_text{
  font-size: 0.7rem;
  margin-top: 10rpx;
  color: #888;
}
.head-icon-item{
  display: flex;
  flex-direction: row;
  padding: 28px 0rpx;
}
.head-icon-item image{
  width: 40rpx;
  height: 40rpx;
}
.head-icon text{
  font-size: 0.7rem;
  padding-left: 8rpx;
  color: #666;
}
.head-icon{
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
  align-self: center;
  flex: 1;
  box-sizing: border-box;
  padding: 0rpx 6rpx;
} 
.connect_btn button{  
   background: #f9ae3d;
   color: #fff; 
   margin: 80rpx 80rpx 60rpx 80rpx;
   font-size: 0.85rem;
   border-radius: 100rpx;
}
.connect_image image{
  width: 180rpx;
  height: 180rpx;
  margin: 10rpx auto;
  display: block;
}
.connect_text{
  padding: 15rpx 0rpx;
  font-size: 0.8rem;
  color: #838383;
  text-align: center;
}

.carts-item {
  display: flex;
  flex-direction: row;
  height: 20%;
  padding: 30rpx;
  /* border-radius: 20rpx; */
  background-color: #ffffff;
  margin:10rpx 28rpx;
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
.carts-item-title{ 
  font-weight: bold;
  margin: 30rpx;
  color: #333;
}
</style>