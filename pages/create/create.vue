<template>
    <view class='page'>
    <view class="create">
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
        <view class="info_cart"> 
        <view class="info_cart_cell">
        <view class="info_cart_label">品牌名称</view>
        <view class="info_cart_input"><input type="text" placeholder="请输入品牌名称"/></view>
        </view>
        <view class="info_cart_cell">
        <view class="info_cart_label">WiFi名称</view>
        <view class="info_cart_input"><input type="text" placeholder="请输入WiFi名称"/></view>
        </view>
        <view class="info_cart_cell">
        <view class="info_cart_label">WiFi密码</view>
        <view class="info_cart_input"><input type="text" placeholder="请输入WiFi密码"/></view>
        </view>
        <view class="tip_text"><image src="../../static/icons/a.svg"></image><text>WiFi密码不会被共享，请放心填写</text></view>
        </view>
        <view class="submit_btn"><button>一键生成WiFi码</button></view>
        </view>
    </view>      
  </template> 
  
  <script>
  export default {
    data() {
      return {};
    },
    onLoad() {},
    methods: {},
  };
  </script> 
  
  <style scoped>
/* pages/create/create.wxss */
.page{
    position: absolute;
    background-color: #f3f3f3;
    height: 100%;
    width: 100%;
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
  .info_cart{
    background-color: #fff;
    border-radius: 20rpx;
    padding: 30rpx;
    margin: 30rpx;
  }
  .info_cart_cell{
    display: flex;
    align-items: center;
    padding: 36rpx 0rpx;
  }
  .info_cart_label{
    width: 180rpx;
  }
  .info_cart_input input{
    margin-left:20rpx ;
    font-weight: bold;
    font-size: 0.9rem;
  }
  .tip_text{
    display: flex;
    align-items: center;
  }
  .tip_text image{
    width: 40rpx;
    height: 40rpx;
    margin-right: 10rpx;
  }
  .tip_text{
    font-size: 0.75rem;
    color: rgb(35, 172, 58);
  }
  .submit_btn{
    margin: 80rpx;
  }
  .submit_btn button{
    background-color: rgb(249, 174, 61);
    color: #fff;
    display: block;
    font-size: 0.85rem;
    width: 100%;
    line-height: 80rpx;
  }
  
  </style>
  