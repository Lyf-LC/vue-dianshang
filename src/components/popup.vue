<template>
<div v-if="flag" class="tanchu">
        <div class="bei" @click="close"></div>
        <div class="kuang" >
            <div class="img">
                <img src="@/assets/images/newsletter.png" alt="">
            </div>
            <div class="youbian">
                <div class="x" @click="close">
                    <svg class="icon" aria-hidden="true">
                        <use xlink:href="#icon-guanbi1"></use>
                    </svg>
                </div>
                <form action="">
                    <h1>订阅简报</h1>
                    <p>订阅<b>Anon</b>以获得最新的产品和更新</p>
                    <input type="email" placeholder="请输入电子邮件地址" required>
                    <button type="submit">订阅</button>
                </form>
            </div>
        </div>
    </div>
</template>

<script>
import {ref} from 'vue'
export default {
    setup(){
        let flag=ref(true)
        function close(){
            flag.value=false
        }
        return {close,flag}
    }
}
</script>

<style lang="less" scoped>
.tanchu {
    position: fixed;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    width: 100%;
    height: 100vh;
    background: hsla(0, 0%, 0%, 0.5);
    z-index: 10;
    display: flex;
    justify-content: center;
    align-items: center;
    opacity: 0;
    z-index: -1;
    animation: chuxian .8s 3s forwards;
    // animation-delay:5s;

    .bei {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
    }

    .kuang {
        overflow: hidden;
        width: 700px;
        height: 400px;
        background: #fff;
        border-radius: 8px;
        display: flex;
        // align-items: center;
        z-index: 5;

        .img {
            width: 400px;
            height: 400px;

            img {
                width: 400px;
                height: 400px;
            }
        }

        .youbian {
            width: 300px;
            position: relative;

            form {
                margin-top: 100px;
                text-align: center;

                h1 {
                    font-size: 18px;
                    margin-bottom: 20px;
                    font-weight: bold;
                }

                p {
                    font-size: 16px;
                    margin-bottom: 20px;
                    color: #787878;
                }

                input {
                    display: block;
                    margin: 0 auto;
                    background-color: transparent;
                    border: 1px solid #454545;
                    font-size: 16px;
                    border-radius: 4px;
                    height: 40px;
                    width: 80%;
                    text-indent: 30px;
                    margin-bottom: 20px;
                }

                button {
                    background-color: #000;
                    color: #fff;
                    padding: 10px 20px;
                    border: none;
                    border-radius: 4px;
                    font-size: 16px;
                    cursor: pointer;
                    font-weight: bold;
                    transition: .2s;

                    &:hover {
                        background-color: #ff8f9c;
                    }
                }
            }

            .x {
                position: absolute;
                top: 10px;
                right: 10px;
                background: #000;
                font-size: 18px;
                font-weight: bold;
                // color: #fff;
                // background-color: #ff8f9c;
                color: #ff8f9c;
                background-color: #fff;
                font-weight: bold;
                padding: 5px 7px;
                border-radius: 8px;
                transition: .2s;
                cursor: pointer;

                &:hover {
                    //     color: #ff8f9c;
                    // background-color: #fff;
                    color: #fff;
                    background-color: #ff8f9c;
                }
            }

        }
    }
}

@keyframes chuxian {
    0% {
        opacity: 0;
        z-index: -1;
        transform: scale(1);
    }

    100% {
        opacity: 1;
        z-index: 10;
        transform: scale(1.1);
    }
}
</style>
