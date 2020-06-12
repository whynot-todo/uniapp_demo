<template>
	<view class="home">
		<swiper indicator-dots circular autoplay indicator-color='rgba(249,180,141,.7)'>
			<swiper-item v-for="item in swipers" :key="item.id">
				<image :src="item.img"></image>
			</swiper-item>
		</swiper>
		<!-- 页面内导航 -->
		<view class="nav">
			<view class="item" v-for="(item,index) in navs" :key="index" @click="navItemClick(item.path)">
				<view :class="item.icons"></view>
				<text>{{item.title}}</text>
			</view>
		</view>
		<!-- 推荐商品 -->
		<view class="hot_goods">
			<view class="tit">推荐商品</view>
			<goods-list  @goodsItemClick="goGoodsDetail" :goods="goods"></goods-list>
		</view>
	</view>
</template>

<script>
	import GoodsList from '../../components/goods-list/goods-list.vue'
	export default {
		data() {
			return {
				swipers: [],
				goods: [],
				navs: [{
						icons: "iconfont icon-ziyuan",
						title: "超市首页",
						path: "/pages/goods/goods"
					},
					{
						icons: "iconfont icon-tupian",
						title: "社区图片",
						path: "/pages/pics/pics"
					},
					{
						icons: "iconfont icon-guanyuwomen",
						title: "联系我们",
						path: "/pages/contact/contact"
					},
					{
						icons: "iconfont icon-shipin",
						title: "学习视频",
						path: "/pages/videos/videos"
					}
				]
			}
		},
		methods: {
			async getSwipers() {
				const res = await this.$myRequest({
					url: '/api/getlunbo'
				})
				this.swipers = res.data.message
			},
			// 获取热门商品列表数据
			async getHotGoods () {
				const res = await this.$myRequest({
					url: '/api/getgoods?pageindex=1'
				})
				this.goods = res.data.message
				console.log(this.goods)
			},
			navItemClick(url) {
				uni.navigateTo({
					url
				})
			},
			goGoodsDetail (id) {
				uni.navigateTo({
					url: '/pages/goods-detail/goods-detail?id='+id
				})
			}
		},
		onLoad() {
			this.getSwipers()
			/* console.log(this.swipers) 得不到相应的数据 */
			this.getHotGoods()
		},
		components:{
			GoodsList
		}
	}
</script>

<style lang="scss">
	swiper {
		width: 100%;
		height: 380rpx;

		image {
			height: 100%;
			width: 100%;
		}
	}

	.nav {
		display: flex;
		align-items: center;

		.item {
			width: 25%;
			text-align: center;

			view {
				background: $shop-color;
				line-height: 120rpx;
				width: 120rpx;
				height: 120rpx;
				border-radius: 90px;
				margin: 10px auto;
			}

			text {
				font-size: 15px;
			}
		}

		.iconfont {
			font-size: 25px;
			color: #fff;
			height: 50px;
		}

		.icon-tupian {
			font-size: 20px;
		}
	}

	.hot_goods {
		background: #eee;

		.tit {
			border-top: 2px solid #eee;
			border-bottom: 2px solid #eee;
			margin-top: 20px;
			margin-bottom: 3px;
			color: $shop-color;
			height: 50px;
			line-height: 50px;
			text-align: center;
			letter-spacing: 20px;
			background: #fff;
		}


	}
</style>
