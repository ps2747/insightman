<template>
    <div class="detection-page">
        <insightman-header-nav></insightman-header-nav>
        <div class="connect-box" v-if="loading">
            <h3>儀器連線</h3>
            <div class="connect-loading">
                <fade-loader color="#B3212D" loading="loading" size="150" sizeUnit="px"></fade-loader>
            </div>
            <h4>正在連線</h4>
            <p>若連線時間過久，請關閉藍芽再重新開啟</p>
        </div>
        <div class="connect-box" v-else>
            <h3>連線成功</h3>
            <img src="/detection/connect-OK.png" alt="">
            <h4>連線完成</h4>
        </div>
        <!-- <insightman-btn title="重新連線" bgColor="#FBEF41" bdColor="black" @click="uploadData()"></insightman-btn> -->
        <button class="ism-button" @click="uploadData()" v-if="loading">重新連線</button>
        <router-link to="/detecting" v-else style="text-decoration: none;">
            <insightman-btn title="開始檢測" bgColor="#FBEF41" bdColor="black"></insightman-btn>
        </router-link>
        <insightman-contact-us></insightman-contact-us>
    </div>
</template>

<script>
import InsightmanHeaderNav from '~/components/InsightmanHeaderNav.vue';
import InsightmanContactUs from '~/components/InsightmanContactUs.vue';
import InsightmanBtn from '~/components/InsightmanBtn.vue';
import Vue from 'vue';
import { VueSpinners } from '@saeris/vue-spinners';
Vue.use(VueSpinners)

export default {
    data:()=>({
        loading: true,
    }),
    components: {
        InsightmanHeaderNav,
        InsightmanContactUs,
        InsightmanBtn,
    },
    methods:{
        async uploadData(){
            setTimeout(()=> {
                this.loading = false;
            }, 2000)    
        },
    },
}
</script>

<style>
@media (max-width: 899px) {
     .connect-box {
        margin: 40px auto; 
        height: 319px;
    }
    .connect-box h3 {
        text-align: center;
        font-size: 25px;
    }
    .connect-box h4 {
        font-size: 41px;
        font-weight: 400;
        color: #B3212D;
        text-align: center;
        margin-bottom: 80px; 
    }
    .connect-box p {
        margin: 0 auto;
        color: #B3212D;
        font-size: 20px;
        width: 80vw;
    }
    .connect-box img {
        display: block;
        margin: 30px auto 10px;
    }
    .connect-loading {
        width: 50px;
        height: auto;
        margin: 30px auto 10px;
    }
    .detection-page .ism-button {
        background: #FBEF41;
    }
}
</style>
