<template>
	<div class="c2f">
		<div class="c1" v-for='(item,index) in data' :key='index' >
			<div class="img">
				<img :src=item.imgSrc  />
			</div>
			<div class="cont">
				<h3>{{item.title}}</h3>
				<div class="top">
					<ico v-for="i in item.num" :key="i" icon="#icon-xingxing2" />
					<ico icon="#icon-xingxing1" v-for="i in (5-item.num)" :key='i' />
				</div>
				<a href="">￥{{item.price}}</a>
			</div>
		</div>
	</div>
</template>

<script>
import ico from '@/components/Ico.vue'
export default {
    props:['data'],
    components:{
        ico
    }
};
</script>

<style lang="less" scoped>
.c2f {
	width: 90%;
	margin: 0 auto;
	height: 90%;
	display: flex;
	flex-direction: column;
	justify-content: space-between;
}

.c1 {
	display: flex;
	justify-content: space-between;
	align-items: center;
	// margin-top: 30px;
	// margin-left: 40px;
	width: 200px;
	height: 70px;
	border-radius: 8px;
	padding: 10px 25px 5px 0;

	img {
		background-color: #ededed;
		border-radius: 4px;
		width: 55px;
		height: 55px;
		padding: 10px;
	}

	.cont {
		h3 {
			font-size: 14px;
			font-weight: bold;
			margin-bottom: 5px;
		}

		a {
			font-size: 16px;
			font-weight: bold;
		}

		width: 110px;
		margin-bottom: 10px;
	}
}
</style>
