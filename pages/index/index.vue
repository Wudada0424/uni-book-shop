<template>
	<view class="content">
		<u-swiper :list="imgList"></u-swiper>
		<u-tabs :list="sortList" :is-scroll="false"  @change="change"></u-tabs>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				imgList: [
					'https://cdn.uviewui.com/uview/swiper/3.jpg',
					'https://cdn.uviewui.com/uview/swiper/2.jpg'
				],
				sortList: [{
					name: '默认'
				}, {
					name: '销量'
				}, {
					name: '推荐',
				},{
					name : '最新商品'
				}]
			}
		},
		async onLoad() {
			// this.$u.get('/api/index').then(res => {
			// console.log(res)
			// })
			// console.log(21213123)

			// await 必须写在async 函数中
			// const res = await this.$u.get('/api/index',)
			// console.log(res)
			// console.log(21213123)


			// const res = await this.$u.get('/api/index', )
			// console.log(res) 
			// const res = await this.$u.post('/api/auth/login',)
			// console.log(res)

			// try {
			// 	const res = await this.$u.post('/api/auth/login',)
			// } catch (e) {

			// }


			// const res = await this.$u.patch('/api/orders/1/confirm',{name : 'Tom'});
			// console.log(res)


			//集中管理api
			// const res = await this.$u.api.index();
			// console.log(res)

			//测试登录
			// const data = {
			// 	email : 'test@a.com',
			// 	password : '123123'
			// }
			// const res = await this.$u.api.authLogin(data )
			// console.log(res)

			// // const ress = await this.$u.api.aaa()
			// // console.log(ress)

			// //测试 vuex
			// console.log(this.vuex_version)

			// // this.$u.vuex('vuex_name' , 'Tom')

			// console.log(this.vuex_name)
		},
		methods: {
			change(index) {
				this.current = index;
			}
		}
	}
</script>

<style lang="scss" scoped>
</style>
