<template>
	<div class="item3">
		<div class="shang">
			<img class="img1" :src=data.imgSrc1 alt="" />
			<img class="img2" :src=data.imgSrc2 alt="" />
		</div>
		<p v-if=data.biaoqian class="biaoqian">{{data.biaoqian}}</p>
		<p v-if=data.xinpin class="biaoqian">新品</p>
		<div class="yidong">
            <a href="" v-for="i in item " :key='i'>
				<ico :icon=i />
			</a>
		</div>
		<div class="xia">
			<a href="">{{data.title}}</a>
			<a href="">{{data.p}}</a>
			<div>
				<ico icon="#icon-xingxing2" v-for="i in data.num" :key="i" />
				<ico icon="#icon-xingxing1" v-for="i in (5 - data.num)" :key="i" />
			</div>
			<p>￥{{data.price}}.00</p>
		</div>
	</div>
</template>

<script>
import ico from '@/components/Ico.vue';
export default {
	components: { ico },
    props:['data'],
    setup(){
        let item=[
            '#icon-shoucang','#icon-xianshi','#icon-repeat','#icon-gouwu'
        ]
        return {item}
    }
};
</script>

<style lang="less" scoped>
.item3 {
	border-radius: 8px;
	border: 1px solid #ddd;
	background: #fff;
	width: 220px;
	display: flex;
	justify-content: space-between;
	flex-direction: column;
	position: relative;
	overflow: hidden;

	.shang {
		margin: 0 auto;
	}

	img {
		width: 210px;
		transition: 0.2s ease;
		// position: absolute;
		transform: scale(0.9);
	}

	.img1 {
		position: absolute;
	}

	.img2 {
		opacity: 0;
	}

	a {
		display: block;
	}

	.yidong {
		position: absolute;
		right: 10px;
		top: 10px;
		transform: translateX(50px);
		opacity: 0;
		transition: 0.2s;
		z-index: 4;

		a {
			padding: 4px;
			border: 1px solid #ddd;
			border-radius: 2px;
			margin-bottom: 5px;
			transition: 0.2s;

			&:hover {
				background: #000;
				color: #fff;
			}
		}

		.icon {
			width: 1.2em;
			height: 1.2em;
		}
	}

	.biaoqian {
		padding: 4px 40px;
		background: green;
		position: absolute;
		top: 0;
		border-radius: 8px;
		color: #fff;
		transform: rotate(-45deg) translate(-30px, -10px);
	}

	.xia {
		display: flex;
		justify-content: space-around;
		flex-direction: column;
		height: 120px;
		padding-bottom: 20px;
		margin-left: 20px;

		:nth-child(1) {
			color: #ff8f9c;
		}

		:nth-child(2) {
			color: #888;
			// font-size: 17px;
		}

		:last-child {
			font-weight: bold;
		}
	}

	&:hover {
		box-shadow: 0 0 10px hsl(0deg 0% 0% / 10%);

		img {
			opacity: 1;
			transform: scale(1);
		}

		.yidong {
			opacity: 1;
			transform: translateX(0px);
		}
	}
}
</style>
