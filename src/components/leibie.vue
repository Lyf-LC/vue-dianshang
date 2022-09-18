<template>
	<section class="cont1">
		<h1>类别</h1>
		<ul>
			<li v-for="(item, index) in data" :key="index">
				<button @click="zhankai(index)">
					<div class="l1">
						<img :src="item.imgSrc" />
						<p>{{ item.title }}</p>
					</div>
					<div>
						<icon :icon="iconName[index]" />
					</div>
				</button>
				<ul :style="{ height: height[index] }" class="ulli" ref="index">
					<li class="lili" v-for="(item, index) in item.child" :key="index">
						<p>{{ item.title }}</p>
						<p>{{ item.price }}</p>
					</li>
				</ul>
			</li>
		</ul>
	</section>
</template>

<script>
import { ref, onMounted, reactive } from 'vue';
import icon from '@/components/Ico.vue';
export default {
	props: ['data'],
	components: {
		icon,
	},
	setup() {
		let iconName = reactive([]);
		let index = ref([]);
		let height = reactive([]);
		function zhankai(i) {
			if (height[i] === '110px') {
				iconName[i] = '#icon-tianjia';
				height[i] = '0px';
				return;
			} else {
					index.value.forEach((item, index) => {
						iconName[index] = '#icon-tianjia';
						height[index] = '0px';
					})
				iconName[i] = '#icon-jian';
				height[i] = '110px';
			}
		}
		onMounted(() => {
			zhankai();
		});
		return { zhankai, height, index, iconName};
	},
};
</script>

<style lang="less" scoped>
.cont1 {
	width: 100%;
	border: 1px solid #ddd;
	border-radius: 8px;

	// height: 500px;
	// background: pink;
	h1 {
		width: 90%;
		font-size: 17px;
		font-weight: bold;
		margin: 10px auto;
	}

	ul {
		width: 90%;
		margin: 0 auto;

		li {
			padding: 5px 0;

			button {
				height: 40px;
				width: 100%;
				outline: none;
				border: none;
				background: none;
				cursor: pointer;
				display: flex;
				justify-content: space-between;
				align-items: center;

				div {
					display: flex;
					justify-content: space-between;
					align-items: center;

					img {
						width: 20px;
						height: 20px;
					}

					p {
						width: 60px;
						text-align: center;
						font-size: 15px;
					}
				}

				.icon {
					width: 1.5em;
					height: 1.5em;
				}
			}
		}
	}

	.ulli {
		height: 0px;
		overflow: hidden;
		transition: 0.5s;
		display: flex;
		justify-content: space-evenly;
		flex-direction: column;
	}

	.lili {
		display: flex;
		justify-content: space-between;
		padding: 4px 0;
	}
}
</style>
