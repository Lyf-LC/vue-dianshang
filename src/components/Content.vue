<template>
	<header class="head">
		<div class="top">
			<div class="w">
				<a href="#" class="logo">
					<img src="@/assets/images/logo/logo.svg" alt="" />
				</a>
				<div class="input">
					<input type="text" placeholder="输入商品名称..." />
					<button>
                        <Icon icon='#icon-sousuo' />
					</button>
				</div>
				<div class="fuwu">
					<a href="#">
                        <Icon icon='#icon-gerenzhongxin' />
					</a>
					<a href="#">
                        <Icon icon='#icon-xihuan' />
						<span>0</span>
					</a>
					<a href="#">
                        <Icon icon='#icon-gouwudai' />
						<span>0</span>
					</a>
				</div>
			</div>
		</div>
		<!-- 标题 -->
		<nav>
			<ul class="zong">
				<li>
					<a class="title" href="#"> 主页 </a>
				</li>
				<li>
					<a class="title" href="#"> 类别 </a>
					<div class="leibie">
						<dl>
							<dt><a href="">电子产品</a></dt>
							<dd><a href="">笔记本电脑</a></dd>
							<dd><a href="">相机</a></dd>
							<dd><a href="">智能手机</a></dd>
							<dd><a href="">平板电脑</a></dd>
							<dd>
								<a href=""
									><img src="@/assets/images/electronics-banner-1.jpg" alt=""
								/></a>
							</dd>
						</dl>
						<dl>
							<dt><a href="">男士服装</a></dt>
							<dd><a href="">夹克</a></dd>
							<dd><a href="">T恤</a></dd>
							<dd><a href="">西装</a></dd>
							<dd><a href="">休闲</a></dd>
							<dd>
								<a href=""
									><img src="@/assets/images/mens-banner.jpg" alt=""
								/></a>
							</dd>
						</dl>
						<dl>
							<dt><a href="">女士用品</a></dt>
							<dd><a href="">休闲</a></dd>
							<dd><a href="">裙子</a></dd>
							<dd><a href="">香水</a></dd>
							<dd><a href="">化妆水</a></dd>
							<dd>
								<a href=""
									><img src="@/assets/images/womens-banner.jpg" alt=""
								/></a>
							</dd>
						</dl>
						<dl>
							<dt><a href="">电子设备</a></dt>
							<dd><a href="">机械键盘</a></dd>
							<dd><a href="">无线鼠标</a></dd>
							<dd><a href="">麦克风</a></dd>
							<dd><a href="">音响</a></dd>
							<dd>
								<a href=""
									><img src="@/assets/images/electronics-banner-2.jpg" alt=""
								/></a>
							</dd>
						</dl>
					</div>
				</li>
				<li>
					<a class="title" href="#"> 男士 </a>
					<div class="kapian">
						<ul>
							<li><a href="">衬衫</a></li>
							<li><a href="">短裤和牛仔裤</a></li>
							<li><a href="">皮鞋</a></li>
							<li><a href="">钱包</a></li>
						</ul>
					</div>
				</li>
				<li>
					<a class="title" href="#"> 女士 </a>
					<div class="kapian">
						<ul>
							<li><a href="">裙子和连衣裙</a></li>
							<li><a href="">耳环</a></li>
							<li><a href="">项链</a></li>
							<li><a href="">化妆工具</a></li>
						</ul>
					</div>
				</li>
				<li>
					<a class="title" href="#"> 珠宝 </a>
					<div class="kapian">
						<ul>
							<li><a href="">耳环</a></li>
							<li><a href="">情侣戒指</a></li>
							<li><a href="">项链</a></li>
							<li><a href="">手镯</a></li>
						</ul>
					</div>
				</li>
				<li>
					<a class="title" href="#"> 香水 </a>
					<div class="kapian">
						<ul>
							<li><a href="">衣服香水</a></li>
							<li><a href="">除臭</a></li>
							<li><a href="">花香味</a></li>
							<li><a href="">空气清新剂</a></li>
						</ul>
					</div>
				</li>
				<li>
					<a class="title" href="#"> 社区 </a>
				</li>
				<li>
					<a class="title" href="#"> 服务中心 </a>
				</li>
			</ul>
		</nav>
        <!-- banner -->
		<div class="banner">
			<swiper
				:autoplay="swiper1.autoplay"
				:loop="swiper1.loop"
				:grabCursor="swiper1.grabCursor"
				class="swiper"
			>
				<swiper-slide>
					<div class="bg1">
						<div class="content">
							<p>秋季新品，焕然衣橱</p>
							<p>女装大甩买</p>
							<p>焕新一折起</p>
							<a href="">现在就去</a>
						</div>
					</div>
				</swiper-slide>
				<swiper-slide>
					<div class="bg2">
						<div class="content">
							<p>流行饰品</p>
							<p>现代太阳镜</p>
							<p>好货推荐</p>
							<a href="">现在就去</a>
						</div>
					</div>
				</swiper-slide>
				<swiper-slide>
					<div class="bg3">
						<div class="content">
							<p>甄选好货，邂逅金秋</p>
							<p>Havva女装疯抢专场</p>
							<p>全球同步，爆款狂欢</p>
							<a href="">现在就去</a>
						</div>
					</div>
				</swiper-slide>
			</swiper>
		</div>
		<div class="item">
			<swiper
				:slidesPerGroup="swiper2.slidesPerGroup"
				:slidesPerView="swiper2.slidesPerView"
				:slidesPerGroupSkip="swiper2.slidesPerGroupSkip"
				:scrollbar="swiper2.scrollbar"
				class="swiper2"
			>
				<swiper-slide
					class="swiper-slide"
					v-for="(item, index) in data.item1"
					:key="index"
				>
					<item :imgSrc="item.imgSrc" :h3="item.h1" :p="item.p" />
				</swiper-slide>
				<div class="swiper-scrollbar"></div>
			</swiper>
		</div>
	</header>
	<div class="neirong">
		<aside class="left">
            <leibie :data="data.item5" />
			<section class="cont2">
				<h1>最畅销的</h1>
                <changxiao :data="data.item6"/>
			</section>
		</aside>
		<div class="right">
			<section class="s1">
				<div class="lan" v-for="(item, index) in data.item2" :key="index">
					<h1>{{ item.title }}</h1>
					<swiper
						:grid="swiper3.grid"
						:scrollbar="swiper3.scrollbar"
						class="swiper3"
					>
						<swiper-slide
							class="swiper-slide"
							v-for="(item, index) in item.content"
							:key="index"
						>
							<item2
								:imgSrc="item.imgSrc"
								:title="item.title"
								:p="item.p"
								:price="item.price"
							/>
						</swiper-slide>
						<div class="swiper-scrollbar"></div>
					</swiper>
				</div>
			</section>
			<section class="s2">
				<h1>每日精选</h1>
				<swiper :scrollbar="swiper4.scrollbar" class="swiper4">
					<swiper-slide class="swiper-slide" v-for="(item,index) in data.item3" :key='index'>
                        <jingxuan :data=item />
                    </swiper-slide>
					<div class="swiper-scrollbar"></div>
				</swiper>
			</section>
			<section class="s3">
				<h1>热销尖货</h1>
				<div class="kapian">
                    <kapian :data="item" v-for="(item,index) in data.item4" :key="index" />
				</div>
			</section>
		</div>
	</div>
    <div class="neironger">
        <div class="top">
            <div class="zuo">
                <h1>资格证书</h1>
                <div class="zhuyao">
                    <img src="@/assets/images/testimonial-1.jpg" alt="">
                    <h3>ALAN DOE</h3>
                    <p>CEO兼创始人</p>
                    <p class="yin">
                        <Icon icon='#icon-quotation'/>
                    </p>
                    <p>始终本着“以信为本,以质取胜”的宗旨，赢得了业界和顾客的一致好评和信任！</p>
                </div>
            </div>
            <div class="zhong">
                <div>
                    <a href="">25%的折扣</a>
                    <h1>夏天新品</h1>
                    <p>商店现在</p>
                    <p>最低￥70</p>
                </div>
            </div>
            <div class="you">
                <h1>我们的服务</h1>
                <div class="zhuyao">
                    <div class="item2">
                        <Icon icon='#icon-boat'/>
                        <div>
                            <p>在时间范围内交付</p>
                            <p>订单超过10万次</p>
                        </div>
                    </div>
                    <div class="item2">
                        <Icon icon='#icon-rocket'/>
                        <div>
                            <p>次日发货</p>
                            <p>仅限内地</p>
                        </div>
                    </div>
                    <div class="item2">
                        <Icon icon='#icon-call'/>
                        <div>
                            <p>最好的在线支持</p>
                            <p>上午8:00至晚上10:00</p>
                        </div>
                    </div>
                    <div class="item2">
                        <Icon icon='#icon-arrow-undo-outline'/>
                        <div>
                            <p>退货政策</p>
                            <p>轻松免费退货</p>
                        </div>
                    </div>
                    <div class="item2">
                        <Icon icon='#icon-ticket-outline'/>
                        <div>
                            <p>七天无理由退货</p>
                            <!-- <p>123456</p> -->
                        </div>
                    </div>
                </div>
            </div>
        </div>
    <div class="buttom">
            <div class="item" v-for='(item,index) in data.item7' :key='index' >
                <img :src=item.imgSrc >
                <div>
                    <a href="">{{item.title}}</a>
                    <a href="">{{item.p}}</a>
                    <p>{{item.date}}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { reactive } from 'vue';
import data from '../../api/商品数据.js';
// 使用swiper的compositon API
import SwiperCore, { Autoplay, Scrollbar, Grid } from 'swiper';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css/bundle';
SwiperCore.use([Autoplay, Scrollbar, Grid]);
import item from '@/components/item.vue';
import item2 from '@/components/item2';
import Icon from '@/components/Ico.vue';
import jingxuan from '@/components/jingXuan.vue'
import kapian from '@/components/kapian.vue'
import leibie from '@/components/leibie.vue'
import changxiao from '@/components/chnagxiao.vue'
export default {
	components: {
		Swiper,
		SwiperSlide,
		item,
		item2,
		Icon,
        jingxuan,
        kapian,
        leibie,
        changxiao
	},
	setup() {
		// swiper相关配置属性放在swiper_options这个变量里
		let swiper1 = reactive({
			autoplay: {
				delay: 5000,
				stopOnLastSlide: false,
				disableOnInteraction: false,
				pauseOnMouseEnter: true,
			},
			grabCursor: true,
			loop: true,
		});
		let swiper2 = reactive({
			autoplay: {
				delay: 2000,
				stopOnLastSlide: false,
				disableOnInteraction: false,
				pauseOnMouseEnter: true,
			},
			slidesPerGroup: 2,
			slidesPerView: 4,
			slidesPerGroupSkip: 2,
			scrollbar: {
				el: '.swiper-scrollbar',
				hide: true,
				draggable: true,
			},
		});
		let swiper3 = reactive({
			grid: {
				fill: 'column',
				rows: 4,
			},
			scrollbar: {
				el: '.swiper-scrollbar',
				hide: true,
				draggable: true,
			},
		});
		let swiper4 = reactive({
			scrollbar: {
				el: '.swiper-scrollbar',
				hide: true,
				draggable: true,
			},
		});
		return { swiper1, swiper2, swiper3, swiper4, data };
	},
};
</script>

<style lang="less" scoped>
.w {
	width: 1330px;
	margin: 0 auto;
	display: flex;
	justify-content: space-between;
}
.head {
	margin-top: 2em;
	margin-bottom: 2em;

	.top {
		height: 70px;
		border-bottom: 1px solid #ddd;

		.logo {
			display: block;
			width: 120px;
		}

		.input {
			position: relative;

			input {
				width: 850px;
				height: 40px;
				border: 1px solid #ddd;
				border-radius: 8px;
				text-indent: 20px;

				&::placeholder {
					letter-spacing: 2px;
				}
			}

			button {
				outline: none;
				border: none;
				background: none;
				width: 30px;
				height: 30px;
				position: absolute;
				top: 6px;
				right: 5px;

				.icon {
					width: 1.5em;
					height: 1.5em;
				}

				&:hover {
					color: #ff8f9c;
					cursor: pointer;
				}
			}
		}

		.fuwu {
			width: 210px;
			display: flex;
			justify-content: space-around;

			a {
				position: relative;

				.icon {
					width: 2.9em;
					height: 2.9em;
				}

				span {
					position: absolute;
					top: -7px;
					right: -10px;
					background-color: red;
					display: block;
					width: 16px;
					height: 16px;
					border-radius: 50%;
					text-align: center;
					line-height: 16px;
					font-size: 12px;
					color: #fff;
				}
			}
		}
	}

	nav {
		.zong {
			width: 950px;
			margin: 0 auto;
			display: flex;
			justify-content: space-around;
			position: relative;

			li {
				position: relative;

				.title {
					display: block;
					font-size: 18px;
					padding: 15px 0;
					font-weight: bold;
					transition: 0.2s;
					position: relative;

					&::after {
						content: '';
						position: absolute;
						bottom: 0;
						left: 0;
						width: 100%;
						height: 3px;
						background-color: pink;
						transition: 0.3s;
						transform: scaleX(0);
						transform-origin: left;
					}

					&:hover {
						color: #ff8f9c;

						&::after {
							transform: scaleX(1);
						}
					}
				}

				&:hover > div {
					opacity: 1;
					transform: translateY(0px);
					z-index: 4;
				}

				.leibie {
					position: absolute;
					top: 53.5px;
					left: -350px;
					width: 1280px;
					height: 340px;
					background: #fff;
					border-radius: 8px;
					box-shadow: 2px 1px 7px 1px #ddd;
					display: flex;
					justify-content: space-around;
					padding: 30px;
					opacity: 0;
					transition: 0.4s;
					transform: translateY(50px);
					z-index: -5;

					dl {
						width: 20%;

						dt {
							font-weight: bold;
							padding: 0 0 10px 0;
							border-bottom: 1px solid #ddd;
							margin-bottom: 5px;
							font-size: 17px;
						}

						dd {
							font-size: 16px;

							padding: 10px 0;
							color: #555;

							img {
								width: 100%;
								border-radius: 8px;
							}

							a:hover {
								color: pink;
							}
						}
					}
				}

				.kapian {
					width: 160px;
					height: 170px;
					position: absolute;
					top: 53.5px;
					left: 0;
					background: #fff;
					box-shadow: 2px 1px 7px 1px #ddd;
					border-radius: 8px;
					opacity: 0;
					transition: 0.3s;
					transform: translateY(50px);
					z-index: -5;

					ul {
						li {
							padding: 10px 0 10px 20px;
						}
					}
				}
			}
		}
	}

	.banner {
		margin: 0 auto 2em;
		width: 1330px;

		.swiper {
			border-radius: 8px;
		}

		.bg1 {
			height: 460px;
			background: url(@/assets/images/banner-1.jpg) no-repeat 25% 75%;
			background-size: cover;
			position: relative;
		}

		.bg2 {
			height: 460px;
			background: url(@/assets/images/banner-2.jpg) 25% 75%;
			background-size: cover;
			position: relative;
		}

		.bg3 {
			height: 460px;
			background: url(@/assets/images/banner-3.jpg);
			background-size: cover;
			position: relative;
		}

		.content {
			position: absolute;
			top: 110px;
			left: 150px;

			:nth-child(1) {
				font-size: 20px;
				color: #ff8f9c;
				margin-bottom: 10px;
			}

			:nth-child(2) {
				font-size: 55px;
				font-weight: bold;
				margin-bottom: 15px;
			}

			:nth-child(3) {
				font-size: 18px;
				color: #787878;
				margin-bottom: 30px;
			}

			:nth-child(4) {
				padding: 10px 30px;
				background: #ff8f9c;
				border-radius: 8px;
				font-weight: bold;
				color: #fff;

				&:hover {
					background: #000;
					color: #fff;
				}
			}
		}
	}

	.item {
		width: 1330px;
		margin: 0 auto;

		.swiper2 {
			width: 100%;
			height: 135px;
		}
	}
}

//内容
.neirong {
	// border: 1px solid red;
	// height: 2430px;
	width: 1330px;
	margin: 0 auto;
	display: flex;
	justify-content: space-between;

	.left {
		width: 25%;
		height: 50%;
		// background: #bfa;
		// display: flex;
		justify-content: space-between;
		flex-direction: column;
		position: sticky;
		top: 0;



		.cont2 {
			margin-top: 20px;
			width: 100%;
			height: 500px;

			// background: yellow;
			h1 {
				width: 90%;
				font-size: 17px;
				font-weight: bold;
				margin: 10px auto 20px;
			}
		}
	}

	.right {
		width: 70%;
		height: 100%;
		// background: #baf;
		display: flex;
		justify-content: space-between;
		flex-direction: column;

		section {
			width: 100%;
		}

		.s1 {
			// background: red;
			display: flex;
			justify-content: space-between;
			height: 560px;

			.lan {
				width: 33%;
				height: 100%;
				// background: #bfa;
				display: flex;
				justify-content: space-between;
				flex-direction: column;

				h1 {
					width: 90%;
					font-size: 20px;
					font-weight: bold;
					// margin-top: 5px;
					padding-bottom: 10px;
					margin-bottom: 30px;
					border-bottom: 1px solid #ddd;
				}

				.swiper3 {
					width: 100%;
					height: 90%;

					.swiper-slide {
						height: 25%;
					}
				}
			}
		}

		.s2 {
			height: 540px;
			display: flex;
			justify-content: space-between;
			flex-direction: column;

			h1 {
				width: 100%;
				height: 10%;
				font-size: 20px;
				font-weight: bold;
				margin-top: 10px;
				padding-bottom: 10px;
				margin-bottom: 30px;
				border-bottom: 1px solid #ddd;
			}

			.swiper4 {
				width: 100%;
				height: 90%;

			}
		}

		.s3 {
			// background: #ffe;
			height: 1200px;

			h1 {
				width: 100%;
				height: 5%;
				font-size: 20px;
				font-weight: bold;
				margin-top: 10px;
				padding-bottom: 10px;
				margin-bottom: 30px;
				border-bottom: 1px solid #ddd;
			}

			.kapian {
				display: flex;
				justify-content: space-between;
				flex-wrap: wrap;
				height: 90%;
				align-content: space-between;
			}
		}
	}
}
.neironger {
    width: 1330px;
    margin: 60px auto 0;
    height: 785px;
    // background:pink;
    display: flex;
    justify-content: space-between;
    flex-direction: column;

    .top {
        width: 100%;
        height: 445px;
        // background: #bfd;
        display: flex;
        justify-content: space-between;

        .zuo {
            width: 23%;
            height: 98%;
            // background:red;
            display: flex;
            justify-content: space-between;
            flex-direction: column;

            h1 {
                width: 100%;
                height: 5%;
                font-size: 20px;
                font-weight: bold;
                // margin-top: 10px;
                padding-bottom: 10px;
                margin-bottom: 30px;
                border-bottom: 1px solid #ddd;

            }

            .zhuyao {
                width: 100%;
                height: 95%;
                margin: 0 auto;
                border: 1px solid #ddd;
                border-radius: 8px;

                img {
                    display: block;
                    width: 100px;
                    height: 100px;
                    // padding: 10px;
                    // background:#000;
                    border-radius: 50%;
                    margin: 30px auto 0;
                    // border: 1px solid #000;
                }

                h3 {
                    width: 150px;
                    text-align: center;
                    font-size: 18px;
                    margin: 20px auto 0;
                    font-weight: bold;
                }

                p {
                    margin: 10px auto 0;
                    width: 150px;
                    text-align: center;
                }

                .yin {
                    font-size: 30px;
                    font-weight: bold;
                    color: pink;

                }
            }
        }

        .zhong {
            width: 49%;
            height: 100%;
            background: url(@/assets/images/cta-banner.jpg);
            background-size: cover;
            border-radius: 8px;
            position: relative;

            div {
                width: 45%;
                height: 50%;
                background: hsla(0, 0%, 100%, 0.7);
                position: absolute;
                top: 0;
                left: 0;
                bottom: 0;
                right: 0;
                margin: auto;
                border-radius: 8px;
                display: flex;
                align-items: center;
                flex-direction: column;
                justify-content: space-evenly;
                padding: 5%;

                a {
                    padding: 3px 10px;
                    background-color: #000;
                    color: #fff;
                    font-weight: bold;
                    font-size: 18px;
                    // margin: 0 auto;
                    // margin-top: 40px;
                    // width: 40%;
                    // display: block;
                    // text-align: center;
                }

                h1 {
                    font-size: 40px;
                    font-weight: bold;
                }

                p {
                    font-size: 18px;
                    color: #787878;
                }

                :last-child {
                    font-weight: bold;
                }
            }
        }

        .you {
            width: 23%;
            height: 98%;
            // background:red;
            display: flex;
            justify-content: space-between;
            flex-direction: column;

            h1 {
                width: 100%;
                height: 5%;
                font-size: 20px;
                font-weight: bold;
                // margin-top: 10px;
                padding-bottom: 10px;
                margin-bottom: 30px;
                border-bottom: 1px solid #ddd;

            }

            .zhuyao {
                width: 100%;
                height: 95%;
                margin: 0 auto;
                border: 1px solid #ddd;
                border-radius: 8px;
                display: flex;
                justify-content: space-evenly;
                flex-direction: column;

                .item2 {
                    display: flex;
                    // justify-content: space-around;
                    align-items: center;
                    // margin-top: 30px;
                    // margin-left: 40px;
                    width: 100%;
                    height: 50px;
                    cursor: pointer;
                    transition: .2s;

                    // border: 1px solid #000;
                    // border-radius: 8px;
                    // padding: 10px 25px 5px 10px;
                    // border: 1px solid #ddd;
                    .icon {
                        font-size: 35px;
                        margin-left: 20px;
                        margin-right: 15px;
                        color: #ff8f9c;
                    }

                    p:first-child {
                        // width: 50%;
                        color:#78787c;
                        font-weight: bold;
                        font-size: 14px;
                        margin-bottom:5px ;
                        letter-spacing: 1px;
                    }

                    &:hover {
                        .icon {
                            color: #000;
                        }
                    }

                }
            }
        }
    }

    .buttom {
        width: 100%;
        height: 290px;
        // background:#bfa;
        display: flex;
        justify-content: space-between;

        .item {
            width: 23%;

            // background: #baf;
            img {
                width: 100%;
                border-radius: 8px;
            }

            div {
                margin-top: 10px;
                width: 100%;

                :nth-child(1) {
                    display: block;
                    margin-bottom: 15px;
                    color: #ff8f9c;
                }

                :nth-child(2) {
                    display: block;
                    font-size: 20px;
                    font-weight: bold;
                    margin-bottom: 15px;

                    &:hover {
                        color: #ff8f9c;
                    }
                }

                :nth-child(3) {
                    font-size: 17px;
                    color: #787878;
                }
            }
        }
    }
}
</style>
