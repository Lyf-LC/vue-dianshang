<template>
	<div class="item2">
		<div class="img">
			<img :src=imgSrc />
		</div>
		<div class="cont">
			<h3>{{title}}</h3>
			<p>{{p}}</p>
			<a href="">{{price}}</a>
		</div>
	</div>
</template>

<script>
export default {
    props:[
        'imgSrc','p','title','price',
    ]
};
</script>

<style lang="less" scoped>
.item2 {
	display: flex;
	justify-content: space-between;
	align-items: center;
	// margin-top: 30px;
	// margin-left: 40px;
	width: 220px;
	height: 70px;
	border-radius: 8px;
	padding: 10px 25px 5px 20px;
	border: 1px solid #ddd;

	img {
		border-radius: 4px;
		width: 80px;
		height: 70px;
		// padding: 10px;
	}

	.cont {
		h3 {
			font-size: 14px;
			font-weight: bold;
			margin-bottom: 5px;
			white-space: nowrap;
			text-overflow: ellipsis;
			overflow: hidden;
		}

		p {
			font-size: 12px;
			margin-bottom: 5px;
		}

		a {
			font-size: 16px;
			font-weight: bold;
		}

		width: 110px;
		margin-bottom: 10px;
	}

	a {
		color: #ff8f9c;
	}
}
</style>
