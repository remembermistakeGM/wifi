<template>
  <view class="admin">
        <view class='page'></view>
        <view class='page_content'>
      <view class='wifi_item' v-for="(item,index) in 10" :key="index"> 
       <view class='wifi_info'>
        <view class='wifi_info_label'>
          <view class='wifi_pp'>Tenda</view>
          <view class='wifi_name'>WiFi名称：你好啊a</view>
          <view class='wifi_num'>昨日有效连接<text>2</text>次</view>
          <view class='wifi_num'>累计有效连接<text>0</text>次</view>
        </view>
        <view class='wifi_info_img'><image src="https://swjls.shuxiaoliu.com/Uploads/image/cache/goods/2022-12-28/63abbb42c5b1b-100x100.png"></image></view>
       </view>
       <view class='bottom_btn'>
        <view class='bottom_button'>
          <svg unregisterModule></svg>
          <image src="../../static/icons/camera.svg"></image><text>打印</text>
        </view>
        <navigator class='bottom_button' url="/pages/share/share"><image src="../../static/icons/settings.svg"></image><text>管理</text></navigator>
        <view class='bottom_button'><image src="../../static/icons/edit.svg"></image><text>修改</text></view>
       </view>
 </view>

</view>
    
    </view>

</template>

<script>
export default {
  name: "adminwifi",
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
  onReachBottom(){
    
  }
}
</script>

<style lang="scss"  scoped>
.page{ 
  position: fixed;
  background-color: #f3f3f3;
  height: 100%;
  width: 100%;
  top: 0;
  z-index: -1;
}


.wifi_item{
  background-color: #fff;
  border-radius: 20rpx;
  padding:30rpx 20rpx;
  margin: 20rpx 36rpx 20rpx 36rpx;
}
.wifi_info{
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.wifi_info_img image{
  width: 140rpx;
  height: 140rpx;
}
.wifi_info_label .wifi_pp{
  font-weight: bold;
  font-size: 0.85rem;
}
.wifi_name{
  margin-top: 10rpx;
  color: #666;
  font-size: 0.75rem;
}
.wifi_num {
  margin-top: 10rpx;
  font-size: 0.75rem;
  color: #666;

}
.wifi_num text{
  color: #000;
  padding: 0rpx 6rpx;
  font-weight: bold;
}
.bottom_btn{
    display: flex;
    margin-top: 30rpx;
}
.bottom_button{
  display: flex;
  align-items: center;
  padding:0rpx 30rpx;
  line-height: 60rpx;
  border-radius: 10rpx;
  border: 1rpx solid #999;
  margin-left: 20rpx;
}
.bottom_button image{
  width: 40rpx;
  height: 40rpx;
}
.bottom_button text{
  font-size: 0.85rem;
  padding-left: 8rpx;
  color:#000;

}
</style>