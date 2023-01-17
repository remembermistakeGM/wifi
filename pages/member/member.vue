<template>
  <view class='wmember'>
    <view class='wmember_bg'></view>
    <view class='grad_bg'>
      <view class='view'>
      <image mode="widthFix" src="/static/images/user.svg"></image>
    </view>
    </view>
    <view class='user-margin'>
    <view class='user_cart'>
      <view class='user_cart_item'>
      <view class='user_head'><image src="https://swjls.shuxiaoliu.com//Uploads/image/goods/2023-01-10/63bcd57f47a90.png"></image></view>
      <view class='user_text'>你好啊</view>
    </view> 
  </view>
    <view class='user_cart' style="margin-top:30rpx">
      <view class='user_cart_title'>
        <view class='user_cart_text'>我的订单</view>
        <view class='user_cart_golink'><text>全部订单</text><image src="../../static/icons/right.svg"></image></view>
      </view>
        <view class='user_cart_group'>
          <navigator class='user_cart_cell'>
            <image src="../../static/icons/member1.svg"></image>
            <text>待付款</text>
          </navigator>
          <navigator class='user_cart_cell'>
            <image src="../../static/icons/member2.svg"></image>
            <text>待发货</text>
          </navigator>
          <navigator class='user_cart_cell'>
            <image src="../../static/icons/member3.svg"></image>
            <text>待收货</text>
          </navigator>
          <navigator class='user_cart_cell'>
            <image src="../../static/icons/member4.svg"></image>
            <text>已完成</text>
          </navigator>
        </view>
    </view>
    <view class='nav_group'>
      <view class='nav_group_child'>
      <navagator class='nav_item'>
        <view class='nav_item_left'><image src="../../static/icons/people.svg"></image><text>我的团队</text></view>
        <image class="remake" src="../../static/icons/right.svg"></image>
      </navagator>
    </view>
    <view class='nav_group_child'>
      <navagator class='nav_item'>
        <view class='nav_item_left'><image src="../../static/icons/folder.svg"></image><text>我的卡包</text></view>
        <image class="remake" src="../../static/icons/right.svg"></image>
      </navagator>
    </view>
      <view class='nav_group_child'>
      <navagator class='nav_item'>
        <view class='nav_item_left'><image src="../../static/icons/headset.svg"></image><text>在线客服</text></view>
        <image class="remake" src="../../static/icons/right.svg"></image>
      </navagator>
    </view>
    <view class='nav_group_child'>

      <navagator class='nav_item'>
        <view class='nav_item_left'><image src="../../static/icons/help-circle.svg"></image><text>帮助中心</text></view>
        <image class="remake" src="../../static/icons/right.svg"></image>
      </navagator>
    </view>
    <view class='nav_group_child'>
      <navagator class='nav_item'>
        <view class='nav_item_left'><image src="../../static/icons/person-add.svg"></image><text>申请团长</text></view>
        <image class="remake" src="../../static/icons/right.svg"></image>
      </navagator>
    </view>

    </view>
    <button class="loginout">退出登录</button>
  </view>
  </view> 
</template>

<script>
export default {
  name: "member",
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
.wmember_bg{
  position: absolute;
  background-color: #f3f3f3;
  height: 100%;
  width: 100%;
  top: 0;
  z-index: -1;
}
.grad_bg{
height: 300rpx;
background: #EFEFBB;  /* fallback for old browsers */
background: linear-gradient(to top, rgb(250, 250, 250), #EFEFBB); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
 position: absolute;
 width: 100%;
 top: 0rpx;

}
.grad_bg .view{
  display: flex;
  justify-content: flex-end;
  
}
.grad_bg image{
  width: 190rpx;
  margin: 60rpx;

} 
 .user_cart{
  background-color: #fff;
  border-radius: 20rpx;
  padding: 20rpx;
 box-shadow: 0rpx 10rpx 20rpx #cecece;
}
.user_cart_item{
  display: flex;
  width: 100%;
  align-items: center;
}
 .user_cart .user_head image{
  width:80rpx;
  height: 80rpx;
  border-radius: 50%;
  margin: 20rpx;
}
.user-margin{
    margin-top:200rpx;
    padding-left: 40rpx;
    padding-right: 40rpx;
    position: absolute;
    width: 100%;
    box-sizing: border-box;
    
}
.user_text{
  padding-left: 30rpx;
  font-weight: bold;
}
.user_cart_title{
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.user_cart_text{
    font-weight: bold;
    font-size: 0.95rem;
}
.user_cart_golink {
  display: flex;
  align-items: center;
  padding-top: 20rpx;
}
.user_cart_golink text{
  color: #666;
  font-size: 0.7rem;
}
.user_cart_golink image{
  width: 30rpx;
  height: 30rpx;
}
.user_cart_group{
  display: flex;
  flex-direction: row;
}
.user_cart_cell{
  flex:1;
  margin: 20rpx 0rpx;
}
.user_cart_cell image{
  width: 60rpx;
  height: 60rpx;
  display: block;
  margin:20rpx auto;
}
.user_cart_cell text{
  display: block;
  font-size: 0.7rem;
  color: #666;
  text-align: center;
}
.nav_group{
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  margin-top: 20rpx;
}
.nav_group .nav_group_child{
  width: 50%;
}
.nav_item{
 display: flex;
 justify-content: space-between;
 border: 1rpx solid #f3f3f3;
 box-sizing: border-box;
 align-items: center;
 background-color: #fff;
 padding: 30rpx 16rpx;
 margin: 20rpx;
 border-radius: 10rpx;
}
.nav_item_left{
  display: flex;
  align-items: center;
}
.nav_item_left image{
  width: 40rpx;
  height: 40rpx;
}
.nav_item_left text{
  color: #666;
  padding-left: 6rpx;
  font-size: 0.8rem;
}
.nav_item .remake{
  width: 36rpx;
  height: 36rpx;
}
.loginout{
  background: #f9ae3d;
  margin: 60rpx;
  line-height: 2rem;
  font-size: 0.85rem;
  color: #fff;
}
</style>