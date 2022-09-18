<template>
	<div class="footer">
		<div class="zhuti1">
			<div class="shang">
				<h1>品牌目录</h1>
				<div class="tiaomu" v-for="(item, index) in data.data1" :key="index">
					<h2>{{ item.title }}</h2>
					<a href="" v-for="(item, index) in item.list" :key="index">{{
						item
					}}</a>
				</div>
			</div>
		</div>
		<div class="zhuti2">
			<div class="zhong">
				<div v-for="(item, index) in data.data2" :key="index">
					<dl>
						<dt>{{ item.title }}</dt>
						<dd v-for="(item, index) in item.list" :key="index">
							<a href="">{{ item }}</a>
						</dd>
					</dl>
				</div>
			</div>
		</div>
		<div class="zhuti3">
			<div class="xia">
				<div>
					<img src="@/assets/images/payment.png" alt="" />
					<p>版权 © lyflc所有</p>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	props: ['data'],
}
</script>

<style lang="less" scoped>
.footer {
	margin-top: 50px;
	height: 730px;
	background: #212121;

	.zhuti1 {
		// width: 1330px;
		height: 37%;
		border-bottom: 1px solid #454545;
		padding-top: 50px;
	}

	.zhuti2 {
		// width: 1330px;
		height: 39%;
		border-bottom: 1px solid #454545;
	}

	.zhuti3 {
		// width: 1330px;
		height: 16%;
	}

	.shang {
		width: 1330px;
		margin: 0 auto;
		// height: 37%;
		height: 100%;
		// background:pink;
		// padding-top: 50px;
		// border-bottom: 1px solid #454545;

		h1 {
			margin-bottom: 20px;
			font-size: 18px;
			font-weight: bold;
			color: #ff8f9c;
		}

		.tiaomu {
			display: flex;
			justify-content: flex-start;
			flex-wrap: wrap;
			column-gap: 20px;
			margin-bottom: 20px;

			h2 {
				font-weight: bold;
				color: #999;
			}

			a {
				color: #707878;
				padding: 0 10px;
				position: relative;
				transition: 0.2s;

				&:not(:last-child)::after {
					position: absolute;
					content: '';
					top: 3px;
					right: -10px;
					width: 1px;
					height: 15px;
					background: #707878;
				}

				&:hover {
					color: #999;
				}
			}
		}
	}

	.zhong {
		// width: 1330px;
		width: 1330px;
		margin: 0 auto;
		// height: 39%;
		// background:red;
		height: 100%;
		display: flex;
		//justify-content: flex-between;
		align-items: center;
		// border-bottom: 1px solid #454545;

		div {
			width: 20%;
			height: 70%;

			dl {
				height: 100%;
				color: #fff;

				dt {
					font-weight: bold;
					font-size: 16px;
					margin-bottom: 20px;
					padding-bottom: 5px;
					position: relative;

					&::after {
						content: '';
						position: absolute;
						width: 50px;
						height: 1px;
						background: #ff8f9c;
						bottom: -5px;
						left: 0;
					}
				}

				dd {
					margin-bottom: 10px;

					a {
						color: #787878;
						transition: 0.2s;

						&:hover {
							color: #ff8f84;
						}
					}
				}
			}
		}
	}

	.xia {
		// width: 1330px;
		width: 1330px;
		margin: 0 auto;
		// height: 16%;
		height: 100%;
		// background: green;
		display: flex;
		justify-content: center;
		align-items: flex-end;

		div {
			padding-bottom: 20px;

			p {
				margin-top: 10px;
				text-align: center;
				color: #787878;
				font-weight: bold;
			}
		}
	}
}
</style>
