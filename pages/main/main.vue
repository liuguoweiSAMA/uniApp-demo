<template>
    <view class="content">
		<view class="page-section swiper">
			<!-- <button @click="getInfo" open-type='getUserInfo'>点击1</button> -->
			<view style="position: relative;" @click="searchPage">
				<image src="../../static/img/search.png" style="width: 32rpx;height: 32rpx;position: absolute;left: 30rpx;top: 24rpx;" mode=""></image>
				<input type="text" placeholder="请输入您的关键字" disabled class="search">
			</view>
			
			<view class="page-section-spacing">
				<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
					<swiper-item>
						<image class="swiper-image" src="../../static/img/tab1.jpg" style="width: 100%;"></image>
					</swiper-item>
					<swiper-item>
						<image class="swiper-image" src="../../static/img/tab2.jpg" style="width: 100%;"></image>
					</swiper-item>
					<swiper-item>
						<image  class="swiper-image" src="../../static/img/tab1.jpg" style="width: 100%;"></image>
					</swiper-item>
				</swiper>
			</view>
			<view class="entrance ">
				<image src="../../static/img/homeIndex1.png" @click="detail" mode=""></image>
				<image src="../../static/img/homeIndex2.png" mode=""></image>
				<image src="../../static/img/homeIndex3.png" mode=""></image>
				<image src="../../static/img/homeIndex4.png" mode=""></image>
			</view>
			<view class="product">
				<view class="ordinal" @click="plush">
					<image src="../../static/img/product1.png" mode=""></image>
					<view class="shop_item">
						<view style="display: inline-block;width: 213px;">
							GON'S旱獭圣诞系列
						</view>
						<view class="price">￥68</view>
					</view>
				</view>
				<view class="ordinal">
					<image src="../../static/img/product2.png" mode="" class="products"></image>
					<image src="../../static/img/title1.png" class="titles"></image>
					<view class="shop_item">
						<view style="display: inline-block;width: 106.56px;">
							GON'S旱獭圣诞系列
						</view>
						<view class="price">￥68</view>
					</view>
				</view>
				<view class="ordinal">
					<image src="../../static/img/product2.png" mode="" class="products"></image>
					<image src="../../static/img/title1.png" class="titles"></image>
					<view class="shop_item">
						<view style="display: inline-block;width: 106.56px;">
							GON'S旱獭圣诞系列
						</view>
						<view class="price">￥68</view>
					</view>
				</view>
				<view class="ordinal">
					<image src="../../static/img/product2.png" mode="" class="products"></image>
					<image src="../../static/img/title1.png" class="titles"></image>
					<view class="shop_item">
						<view style="display: inline-block;width: 106.56px;">
							GON'S旱獭圣诞系列
						</view>
						<view class="price">￥68</view>
					</view>
				</view>
				<view class="ordinal">
					<image src="../../static/img/product2.png" mode="" class="products"></image>
					<image src="../../static/img/title1.png" class="titles"></image>
					<view class="shop_item">
						<view style="display: inline-block;width: 106.56px;">
							GON'S旱獭圣诞系列
						</view>
						<view class="price">￥68</view>
					</view>
				</view>
			</view>
		</view>
    </view>
</template>
<style lang='scss'>
	*{
		margin: 0;
		padding:  0 0;
	}
	body,html{
		width: 100%;
		height: 100%;
		/* overflow: hidden; */
	}
	.entrance{
		/* margin-top: 14px; */
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		flex-wrap: wrap;
	   
		image{
			width: 330rpx;
			height: 188rpx;
			margin-top: 14px;
		}
	}
	.product{
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		flex-wrap: wrap;
		.ordinal{
			margin-top: 11px;
			display: flex;
			width: 330rpx;
			/* height: 202px; */
			flex-direction: column;
			font-size: 12px;
			font-weight:600;
			position: relative;
			/* background: red; */
			background: url('https://cdn.lljgame.com/wechat_carnival/index_bg.png') no-repeat;
			 background-size: cover;
			.shop_item{
				padding-left: 7.68px;
			}
			.titles{
				position: absolute;
				right: 0;
				top: -10px;
				width: 60rpx;
				height: 124rpx;
			}
			.price{
				position: absolute;
				right: 16rpx;
				top: 328rpx;
				font-size: 30rpx;
				color: #FB007E;
			}
			image{
				width: 330rpx;
				height: 316.8rpx;
				margin-bottom: 16rpx;
			}
		}
	}
	.content{
		padding: 0 14.4px;
		background: white;
		width: 100%;
		height: 100%;
	}
	.swiper-image{  
	     width:100%;  
		 border-radius: 10px;
	     /* height:300upx; */
	 }
	 .search{
		 /* border-image:linear-gradient(90deg, rgba(251,0,126,1), rgba(253,109,126,1)) 1 1; */
		background:rgba(255,255,255,1);
		border-radius:20px;
		margin-bottom: 15px;
		border:1px solid #FB007E; 
		font-size: 24rpx;
		height: 80rpx;
		padding-left: 82rpx;
		margin-top: 19.2px;
	 }
	.ser-input{
		border: 1px solid pink;
		border-radius: 25px;
		font-size: 10px;
	}
</style>
<script>
    import {
        mapState
    } from 'vuex'

    export default {
		data(){
		  return {
			  indicatorDots: true,
			  autoplay: true,
			  interval: 2000,
			  duration: 500
		  }
		},
        computed: mapState(['forcedLogin', 'hasLogin', 'userName']),
		methods:{
			searchPage: async function(e) {
				uni.navigateTo({
					url: '/pages/search/search'
				})
				// this.$api.msg('点击了搜索框');
			},
			detail: async function() {
				uni.navigateTo({
					url: '/pages/detail/detail'
				})
			},
			plush: async function () {
				uni.navigateTo({
					url: '/pages/plush/plush'
				})
			},
			getInfo: async function () {
				let that = this
				// let globalData = getApp().globalData
			// 	uni.login({
			// 		  provider: 'weixin',
			// 	      success: res_login => {
			// 		    getApp().globalData.openId = res_login.code
			// 			// globalData.openId = res_login.code
			// 	        console.log('-------获取code-------')
			// 		    console.log(res_login)
			//              uni.getUserInfo({
			// 				provider: 'weixin',
			// 				success: function(infoRes) {
			// 					// getApp().globalData.errcode = 0
			// 					// let globalData = getApp().globalData
			// 					let params = {
			// 						userInfo: infoRes
			// 					}
			// 					uni.request({
			// 						url: 'https://online.lljgame.com/api/carnival/user/wx/login',
			// 					    data: params,
			// 						method:'POST',
			// 					    success: (res) => {
			// 					        console.log(res);
			// 					    },fail(val) {
			// 					    	console.log(val)
			// 					    }
			// 					});
			// 				},fail(res) {
			// 					console.log(res)
			// 				}
			// 			});
			// 	      }
			// 	});
			}
		},
		
		onShow() {
			uni.setTabBarItem({
				index: 0,
				"text": "首页",
				"iconPath": "static/img/hidden_index1.png",
				"selectedIconPath": "static/img/hidden_index2.png"
			})
			uni.setTabBarItem({
			  index: 1,
			  "text": "娃柜",
			  "iconPath": "static/img/hidden_case1.png",
			  "selectedIconPath": "static/img/hidden_case2.png"
			})
			uni.setTabBarItem({
			  index: 2,
			  "text": "我的",
			  "iconPath": "static/img/hidden_user1.png",
			  "selectedIconPath": "static/img/hidden_user2.png"
			})
			uni.setTabBarStyle({
			  color: '#FF0000',
			  selectedColor: '#FB007E',
			  backgroundColor: '#FFFFFF',
			  borderStyle: 'white'
			})
		},
        onLoad() {
			this.getInfo()
			
			// uni.getUserInfo({
			// 	provider: 'weixin',
			// 	success: function(infoRes) {
			// 		globalData.errcode = 0
			// 		// globalData.userInfo = userInfo
			// 		let params = {
			// 			userInfo : globalData
			// 		}
			// 		uni.request({
			// 			url: 'api/user/wx/login', //仅为示例，并非真实接口地址。
			// 			data: params,
			// 			method:'POST',
			// 			success: (res) => {
			// 				console.log(res);
			// 			}
			// 		});
			// 	},fail(res) {
			// 		console.log(res)
			// 	}
			// });
			// var globalData = getApp().globalData.url
			// let params = {
			// 	pi: '1',
			// 	ps: '10'
			// }
			
			// uni.request({
			//     url: 'api/carnival', //仅为示例，并非真实接口地址。
			//     data: params,
			// 	method:'GET',
			//     success: (res) => {
			//         console.log(res);
			//     }
			// });
       //      if (!this.hasLogin) {
       //          uni.showModal({
       //              title: '登录',
       //              content: '您未登录，需要登录后才能继续',
       //              /**
       //               * 如果需要强制登录，不显示取消按钮
       //               */
       //              showCancel: !this.forcedLogin,
       //              success: (res) => {
       //                  if (res.confirm) {
							// /** 
							//  * 如果需要强制登录，使用reLaunch方式
							//  */
       //                      if (this.forcedLogin) {
       //                          uni.reLaunch({
       //                              url: '../login/login'
       //                          });
       //                      } else {
       //                          uni.navigateTo({
       //                              url: '../login/login'
       //                          });
       //                      }
       //                  }
       //              }
       //          });
       //      }
        }
    }
</script>

<style>
    .hello {
        display: flex;
        flex: 1;
        flex-direction: column;
    }

    .title {
        color: #8f8f94;
        margin-top: 50upx;
    }

    .ul {
        font-size: 30upx;
        color: #8f8f94;
        margin-top: 50upx;
    }

    .ul>view {
        line-height: 50upx;
    }
</style>
