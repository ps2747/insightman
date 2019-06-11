<template>
    <div class="ism-header">
        <!-- <div class="ism-header-hamburger" @click="showMenu()">
            <img src="/header-hamburger.png" alt="" v-if="!show">
            <img src="/header-hamburger-open.png" alt="" v-else>
        </div>
        <router-link to="/">
            <div class="ism-header-logo">
                <img src="/header-logo.png" alt="">
            </div>
        </router-link>
        <div class="ism-header-hamburger">
            <img src="/header-earth.png" alt="" v-if="!show">
            <img src="/header-earth-open.png" alt="" v-else>
        </div>
        <div class="ism-header-menu" :class="showOrNot"></div> -->
        <div class="ism-header-hamburger" @click="showMenu()">
            <img src="/header-hamburger.png" alt="" v-if="!show">
        </div>
        <router-link to="/">
            <div class="ism-header-logo">
                <img src="/header-logo.png" alt="">
            </div>
        </router-link>
        <div class="ism-header-hamburger" @click="SelectLanguage()">
            <img src="/header-earth.png" alt="" v-if="!show">
        </div>
        <div class="ism-header-menu" :class="showOrNot">
            <div class="ism-header">
                <div class="ism-header-hamburger" @click="showMenu()">
                    <img src="/header-hamburger-open.png" alt="" v-if="show">
                </div>
                <router-link to="/">
                    <div class="ism-header-logo" @click="showMenu()">
                        <img src="/header-logo.png" alt="">
                    </div>
                </router-link>
                <div class="ism-header-hamburger" @click="SelectLanguage(),showMenu()">
                    <img src="/header-earth-open.png" alt="" v-if="show">
                </div>
            </div>
            <div class="ism-header-menu-content">
                <li>首頁</li>
                <li>旗下品牌</li>
                <li>公司簡介</li>
                <li>產品介紹</li>
                <li>排廢檢測</li>
                <li>線上商城</li>
                <li>經銷據點</li>
                <li>聯絡我們</li>
                <insightman-btn title="會員中心" bgColor="#FBEF41" bdColor="black"></insightman-btn>
            </div>
        </div>
        <div class="ism-header-select" :class="selectOrNot">
            <div class="ism-header">
                <div class="ism-header-hamburger" @click="SelectLanguage()">
                    <img src="/header-hamburger-open.png" alt="">
                </div>
                <router-link to="/">
                    <div class="ism-header-logo" @click="showMenu()" >
                        <img src="/header-logo.png" alt="">
                    </div>
                </router-link>
                <div class="ism-header-hamburger" @click="SelectLanguage()" >
                    <img src="/header-earth-open.png" alt="" >
                </div>
            </div>
            <div class="ism-header-menu-content">
                <li>繁體中文</li>
                <li>簡體中文</li>
                <li style="margin-bottom:25vh;">English</li>
                <insightman-btn title="註冊/登入" bgColor="#FBEF41" bdColor="black" ></insightman-btn>
            </div>
        </div>
    </div>
</template>

<script>
import InsightmanBtn from '~/components/InsightmanBtn.vue';
export default {
    data:() => ({
        show: false,
        select: false,
    }),
    components:{
        InsightmanBtn,
    },
    methods :{
        showMenu(){
            this.show = !this.show
        },
        SelectLanguage(){
            this.select = !this.select
        },
    },
    computed:{
        showOrNot(){
            return this.show ? 'open':'';
        },
        selectOrNot(){
            return this.select ? 'open':'';
        }
    }
}
</script>

<style>
@media (max-width: 899px) {
    .ism-header {
        position: relative;
        width: 100vw;
        height: 70px;
        /* background: red;  */
        display: inline-flex;
        justify-content: space-around;
        align-items: center;
    }
    .ism-header-logo img {
        height: 40px;
    }
    .ism-header-menu,.ism-header-select {
        display: none; 
        transition: .3s;
    }
    .ism-header-hamburger {
        width: 25px;
        height: 25px;
    }
    /* .ism-header-hamburger,.nuxt-link-active {
        z-index: 999;
    } */
    .ism-header-menu.open,.ism-header-select.open {
        display: block;
        position: fixed;
        width: 100%;
        height: 100%;
        background-color: #707070;
        top: 0;
        left: 0;
        transition: .3s;
        opacity: 1;
    }
    .ism-header-menu.open {
        z-index: 900;
    }
    .ism-header-select.open {
        z-index: 901;
    }
    .ism-header-menu-content {
        width: 80vw;
        height: 80vh;
        margin: 3vh auto 5vh ;
        text-align: center;
    }
    .ism-header-menu-content li {
        list-style-type: none;
        margin: 0;
        font-size: 20px;
        color: #fff;
        margin-bottom: 3vh;
    }
    .ism-header-select.open .ism-header-menu-content {
        height: 50vh;
        margin: 20vh auto 5vh;
    }
}
</style>
