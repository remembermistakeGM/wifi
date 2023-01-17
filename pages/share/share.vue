<template>
  <view class='share page'>
    <view class='pagebg'></view>
    <view class='share_cart'>
      <view class='share_cart_text1'>用户连接WiFi可产生收益</view>
      <view class='share_cart_text2'>用户连接WiFi可产生收益</view>
      <view class='share_cart_image'><image mode="widthFix" src="https://swjls.shuxiaoliu.com/Uploads/image/cache/goods/2022-12-28/63abbb42c5b1b-100x100.png"></image></view>
      <view class='share_cart_bottom'>
        <view class='share_cart_text3'>用户连接WiFi可产生收益</view>
        <view class='share_cart_text4'>用户连接WiFi可产生收益</view>
      </view>
    </view> 
    <view class='share_cart_text5'>用户连接WiFi可产生收益</view>

    <view class='bb_btn'>
     <view class='bb_btn_cart'>
      <image src="../../static/icons/pic.svg"></image>
      <text>海报下载</text>
     </view>
     <view class='bb_btn_cart'>
      <image src="../../static/icons/wechat.svg"></image>
      <text>海报下载</text>
     </view>
     <view class='bb_btn_cart'>
      <image src="../../static/icons/settings-white.svg"></image>
      <text>海报下载</text>
     </view>
    </view> 
    
    <!-- <u-action-sheet :list="list" v-model="show" :tips="tips" :cancel-btn="true"></u-action-sheet> -->
  </view>
</template>

<script>
export default {
  name: "share",
  components: {},
  props: {},
  data() {
    return {
   
    }
  },
  computed: {},
  methods: {},
  watch: {},

  // 页面周期函数--监听页面加载
  onLoad() {

  },
  // 页面周期函数--监听页面初次渲染完成
  onReady() {},
  // 页面周期函数--监听页面显示(not-nvue)
  onShow() {},
  // 页面周期函数--监听页面隐藏
  onHide() {},
  // 页面周期函数--监听页面卸载
  onUnload() {},

} 
</script>

<style scoped>


.pagebg{ 
  position: fixed;
  background-color: #f3f3f3;
  height: 100%;
  width: 100%;
  top: 0;
  z-index: -1;
}
.share_cart{
  background-color: #fff;
  margin: 40rpx;
  border-radius: 18rpx;
  box-shadow: 0 20rpx 20rpx #e4e4e4;
}
.share_cart_text1{
  font-size: 0.7rem;
  padding-top: 40rpx;
  text-align: center;
}
.share_cart_text2{
  font-size: 0.7rem;
  margin-top: 40rpx;
  color: #999;
  text-align: center;

}
.share_cart_image image{
  width:70%;
  margin-left: 15%;
  margin-top: 50rpx;
}
.share_cart_bottom{
  background: #f9ae3d;
  height: 140rpx;
  border-bottom-left-radius: 18rpx;
  border-bottom-right-radius: 18rpx;

}
.share_cart_text3{
  font-size: 0.7rem;
  margin-top: 40rpx;
  color: #fff;
  text-align: center;
  padding-top: 30rpx;
}
.share_cart_text4{
  font-size: 0.7rem;
  margin-top: 20rpx;
  color: #fff;
  text-align: center;
}
.share_cart_text5{
  text-align: center;
  color: #666;
  font-size: 0.8rem;

}
.bb_btn {
  display: flex;
  flex-direction: row;
  justify-content: center;
  margin: 50rpx;
}
.bb_btn .bb_btn_cart{
  flex: 1;
  align-self: center;  
}
.bb_btn .bb_btn_cart image{
  width:50rpx;
  height: 50rpx;
  display: block;
  padding: 30rpx;
  margin: 20rpx auto;
}
.bb_btn .bb_btn_cart:nth-child(1) image{
  background-color: rgb(13, 72, 184);
  border-radius: 100%;
}
.bb_btn .bb_btn_cart:nth-child(2) image{
  background-color: rgb(33, 216, 110);
  border-radius: 100%;
}
.bb_btn .bb_btn_cart:nth-child(3) image{
  background-color: #f9ae3d;
  border-radius: 100%;
}
.bb_btn .bb_btn_cart text{
  text-align: center;
  display: block;
  color: #666;
  font-size: 0.9rem;
}
</style>