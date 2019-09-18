<template>
    <div class="ism-header" >
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
        <router-link :to="check_lang + '/'">
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
                    <img src="/header-hamburger-new-open.png" alt="" v-if="show">
                </div>
                <div class="ism-header-logo" @click="showMenu()">
                        <img src="/header-logo.png" alt="">
                </div>
                <div class="ism-header-hamburger" @click="SelectLanguage(),showMenu()">
                    <img src="/header-earth.png" alt="" v-if="show">
                </div>
            </div>
            <div class="ism-header-menu-content">
                <li @click="$router.push(check_lang + '/') & showMenu()">{{$t('menu_index')}}</li>
                <!-- <li>旗下品牌</li> -->
                <li @click="$router.push(check_lang + '/about') & showMenu()">{{$t('menu_about')}}</li>
                <li @click="$router.push(check_lang + '/product-gmg') & showMenu()">{{$t('menu_gmg')}}</li>  
                <li @click="$router.push(check_lang + '/product-engine-wizard') & showMenu()">{{$t('menu_engine')}}</li>  
                <!-- <li @click="$router.push('/checkhold') & showMenu()">排廢檢測</li> -->
                <!-- <li @click="$router.push('/shop') & showMenu()">線上商城</li> -->
                <li @click="selectTaiwanHold">{{$t('menu_mall_tw')}}</li>
                <li @click="selectAsiaHold">{{$t('menu_mall_asia')}}</li>
                <li @click="$router.push(check_lang + '/contact') & showMenu()">{{$t('menu_contact')}}</li>
                <!-- <router-link to="/member" style="text-decoration: none;">
                    <insightman-btn title="會員中心" bgColor="#FBEF41" bdColor="black"></insightman-btn>
                </router-link> -->
            </div>
        </div>
        <div class="ism-header-select" :class="selectOrNot">
            <div class="ism-header">
                <div class="ism-header-hamburger" @click="SelectLanguage()">
                    <img src="/header-hamburger-new-open.png" alt="">
                </div>
                <div class="ism-header-logo" @click="SelectLanguage()" >
                        <img src="/header-logo.png" alt="">
                </div>
                <div class="ism-header-hamburger" @click="SelectLanguage()" >
                    <img src="/header-earth.png" alt="" >
                </div>
            </div>
            <div class="ism-header-menu-content">
                <li @click="switchTW">繁體中文</li>
                <li @click="switchCN">简体中文</li>
                <li style="margin-bottom:25vh;">English</li>
                <!-- <insightman-btn title="註冊/登入" bgColor="#FBEF41" bdColor="black" ></insightman-btn> -->
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
        check_lang : '',
    }),
    mounted(){
        if(this.$i18n.locale == 'CN') {
            this.check_lang = '/CN'
        } else {
            this.check_lang = ''
        }
        // console.log(this.check_lang)
    },
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
        selectTaiwanHold(){
            this.$router.push(this.check_lang + '/waiting') ;
            this.showMenu();
            sessionStorage['select_area'] = '1'
        },
        selectAsiaHold(){
            // console.log(this.check_lang)
            this.$router.push(this.check_lang + '/waiting') ;
            this.showMenu();
            sessionStorage['select_area'] = '2'
        },
        switchCN(){
            if(this.$i18n.locale == 'CN') {
                this.SelectLanguage()
            } else {
                this.$router.push('/CN' + location.pathname)
                this.SelectLanguage()
                this.check_lang = '/CN'
            }
        },
        switchTW(){
            let path = location.pathname
            if(location.pathname == '/CN') {
                path = path.replace('/CN','/')
                if(this.$i18n.locale == 'CN') {
                    this.$router.push(path)
                    this.SelectLanguage()
                } else {
                    this.SelectLanguage()
                }
            } else {
                this.check_lang = ''
                path = path.replace('/CN','')
                if(this.$i18n.locale == 'CN') {
                    this.$router.push(path)
                    this.SelectLanguage()
                } else {
                    this.SelectLanguage()
                }
            }

            
        }
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
        background: #fff;
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
        display: flex;
        align-items: center;
        justify-content: center;
    }
    /* .ism-header-hamburger,.nuxt-link-active {
        z-index: 999;
    } */
    .ism-header-menu.open,.ism-header-select.open {
        display: block;
        position: fixed;
        width: 100%;
        height: 100%;
        background-color: #FFF;
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
        margin: 5vh auto 5vh ;
        text-align: center;
    }
    .ism-header-menu-content li {
        list-style-type: none;
        margin: 0;
        font-size: 20px;
        color: #000;
        margin-bottom: 3vh;
    }
    .ism-header-select.open .ism-header-menu-content {
        height: 50vh;
        margin: 20vh auto 5vh;
    }
}
</style>
