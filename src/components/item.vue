<template>
	<div class="item1">
		<div>
			<img :src=imgSrc alt="" />
		</div>
		<div class="cont">
			<div class="cont1">
				<h3>{{h3}}</h3>
				<p>{{p}}</p>
			</div>
			<a href="">显示所有</a>
		</div>
	</div>
</template>

<script>
export default {
    props:[
        'imgSrc','h3','p'
    ]
};
</script>

<style lang='less' scoped>
.item1 {
	display: flex;
	justify-content: space-between;
	align-items: center;
	margin-top: 30px;
	margin-left: 40px;
	width: 220px;
	height: 70px;
	border-radius: 8px;
	padding: 10px 25px 5px 10px;
	border: 1px solid #ddd;

    img {
		border-radius: 4px;
		background: #ddd;
		width: 30px;
		height: 30px;
		padding: 10px;
	}

	.cont1 {
		width: 110px;
		display: flex;
		justify-content: space-between;
		margin-bottom: 10px;
	}

	a {
		color: #ff8f9c;
	}
}
</style>
