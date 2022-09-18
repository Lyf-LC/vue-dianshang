<template>
	<header>
		<div class="w">
			<ul>
				<li>
					<a href="#">
						<Icon icon="#icon-lianshu"/>
					</a>
				</li>
				<li>
					<a href="#">
                        <Icon icon="#icon-tuite1"/>
					</a>
				</li>
				<li>
					<a href="#">
                        <Icon icon="#icon-icon_xiangji-mian"/>
					</a>
				</li>
				<li>
					<a href="#">
                        <Icon icon="#icon-linkedin-fill"/>
					</a>
				</li>
			</ul>
			<p><span>FREE SHIPPING</span> THIS WEEK ORDER OVER - $55</p>
			<div class="right">
				<select>
					<option value="0">RMB ￥</option>
					<option value="0">USD $</option>
					<option value="1">EUR €</option>
				</select>
				<select>
					<option value="0">简体中文</option>
					<option value="1">English</option>
				</select>
			</div>
		</div>
	</header>
</template>

<script>
import Icon from "@/components/Ico.vue"
export default {
    components: {Icon}
};
</script>

<style lang="less" scoped>
header {
	margin-top: 1em;
	height: 50px;
	border-bottom: 1px solid #ddd;

	.w {
		width: 1330px;
		margin: 0 auto;
		display: flex;
		justify-content: space-between;
	}

	ul {
		li {
			display: inline-block;

			a {
				color: #666;
				background-color: #f2f2f2;
				border-radius: 8px;
				display: block;
				padding: 5px;
				transition: all 0.2s;
                margin-left: 5px;
                // font-size: 20px;

				.icon {
                    // font-size: 14px;
					width: 1.2em;
					height: 1.2em;
				}

				&:hover {
					color: #fff;
					background-color: #ff8f9c;
				}
			}
		}
	}

	p {
		color: #888;
		font-size: 13px;

		span {
			font-weight: 600;
		}
	}

	.right {
		// margin-right: 50px;
		select {
			font-size: 17px;
			color: #888;
			outline: none;
			border: none;
			margin-left: 10px;
			min-width: 80px;

			option {
				outline: none;
				border: none;
			}
		}
	}
}
</style>
