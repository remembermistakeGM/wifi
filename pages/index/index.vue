<template>
  <view class="container1">
    <view class="swiper1">
      <image
        style="width: 100%"
        src="https://swjls.shuxiaoliu.com//Uploads/image/goods/2022-08-10/62f3436390580.jpg"
      ></image>
    </view>
    <view class="index_cart">
      <navigator class="index_cart_item" url="/pages/create/create">
        <image
          class="index_cart_image overheight"
          src="/static/images/index_wifi1.svg"
        ></image> 
        <view class="index_cart_label">
          <text class="text1">创建WiFi码</text>
          <text class="text2">一件连接·安全蹭网</text>
        </view>
      </navigator>
      <navigator class="index_cart_item" url="/pages/adminwifi/adminwifi"> 
        <image
          class="index_cart_image"
          src="/static/images/index_wifi2.svg"
        ></image>
        <view class="index_cart_label">
          <text class="text1">我的WiFi码</text>
          <text class="text2">查看管理WiFi码</text>
        </view>
      </navigator>
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

  .index_cart{
	display: flex;
  }
  .index_cart_item{
	flex: 1;
	display: flex;
	flex-direction: row;
	align-items: center;
	background-color: #f9ae3d;
	margin: 20rpx;
	border-radius: 16rpx;
	padding: 16rpx;
   
  }
  .index_cart_image{
	width: 100rpx;
	height: 100rpx;
	display: block;
  }
  .overheight{
	height: 80rpx;
  }
  .index_cart_label{
	padding-left:12rpx ;
  }
  .index_cart_label text{
	display: block;
	color: #fff;
  } 
  .index_cart_label .text1{
	font-weight: bold;
	font-size: 0.9rem;
  }
  .index_cart_label .text2{
	font-size:20rpx;
	padding-top: 10rpx;
  }

</style>
