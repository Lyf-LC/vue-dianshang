<template>
	<div class="s4i">
		<div class="left2">
			<img :src=data.imgSrc alt="" />
		</div>
		<div class="right2">
			<div class="top">
                <ico icon='#icon-xingxing2' v-for='i in data.num' :key='i' />
				<ico icon='#icon-xingxing1' v-for='i in (5-data.num)' :key='i' />
			</div>
			<a href="" class="t1">{{data.title}}</a>
			<p class="p1">{{data.p}}</p>
			<p class="p2">￥{{data.price}}.00</p>
			<a href="" class="bt">添加至购物车</a>
			<div class="f1">
				<span>已卖出 <b>{{data.sold}}</b></span>
				<span>还剩 <b>{{data.zong-data.sold}}</b></span>
			</div>
			<progress :value='data.sold' :max="data.zong"></progress>
			<p>限时秒杀：</p>
			<div class="miaosha">
				<div>
					<span>360</span>
					<span>天</span>
				</div>
				<div>
					<span>24</span>
					<span>小时</span>
				</div>
				<div>
					<span>59</span>
					<span>分钟</span>
				</div>
				<div>
					<span>00</span>
					<span>秒</span>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import ico from '@/components/Ico.vue'
export default {
    props:[
        'data'
    ],
    components:{ico}
};
</script>

<style lang="less" scoped>
.s4i {
	display: flex;
	justify-content: space-around;

	.left2 {
		width: 40%;
		margin-top: 20px;

		img {
			width: 100%;
		}
	}

	.right2 {
		width: 50%;

		.top {
			margin-bottom: 15px;
            .icon{
                margin-left: 3px;
            }
		}

		.t1 {
			display: block;
			font-size: 20px;
			font-weight: bold;
			margin-bottom: 10px;
		}

		.p1 {
			color: #818181;
			margin-bottom: 10px;
		}

		.p2 {
			margin-bottom: 20px;
			font-size: 20px;
			color: #ff8f9c;
			font-weight: bold;
		}

		.bt {
			display: inline-block;
			padding: 10px 20px;
			font-size: 20px;
			font-weight: bold;
			background: #ff8f9c;
			color: #fff;
			border-radius: 4px;
			transition: 0.4s;
			margin-bottom: 20px;

			&:hover {
				background: #000;
			}
		}

		.f1 {
			display: flex;
			justify-content: space-between;
		}

		progress {
			margin-left: 3px;
			margin-top: 10px;
			margin-bottom: 20px;
			// border: 3px solid #ededed;
			outline: 3px solid #ededed;
			width: 99%;
			height: 4px;
			border-radius: 8px;
			background-color: orange;

			&::-webkit-progress-bar {
				background-color: #ededed;
			}

			&::-webkit-progress-value {
				background-color: pink;
			}
		}

		.miaosha {
			width: 70%;
			margin-top: 20px;
			display: flex;
			justify-content: space-around;

			div {
				width: 70px;
				height: 70px;
				border-radius: 8px;
				background: #ededed;
				display: flex;
				justify-content: space-evenly;
				align-items: center;
				flex-direction: column;

				:first-child {
					font-weight: bold;
					font-size: 25px;
				}

				:last-child {
					font-size: 12px;
				}
			}
		}
	}
}
</style>
