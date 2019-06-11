<template>
    <div class="detecting-page">
        <insightman-header-nav></insightman-header-nav>
        <div class="detecting" v-if="loading">
            <h3>進行檢測</h3>
            <h4>第一次靜態加速</h4>
            <img src="/detection/speedometer.png" alt="">
        </div>
        <div class="detecting" v-if="!loading">
            <h3>進行檢測</h3>
            <h4>第二次靜態加速</h4>
            <img src="/detection/speedometer.png" alt="">
        </div>
        <button class="ism-button" @click="oneMoreTime()" v-if="loading">下一步</button>
        <router-link to="/ReportDetection" v-else style="text-decoration: none;">
            <insightman-btn title="檢測報告" bgColor="#FBEF41" bdColor="black"></insightman-btn>
        </router-link>
        <insightman-contact-us></insightman-contact-us>
    </div>
</template>

<script>
import InsightmanHeaderNav from '~/components/InsightmanHeaderNav.vue';
import InsightmanContactUs from '~/components/InsightmanContactUs.vue';
import InsightmanBtn from '~/components/InsightmanBtn.vue';


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
        async oneMoreTime(){
            setTimeout(()=> {
                this.loading = false;
            }, 2000)    
        },
    },
}
</script>

<style>
@media (max-width:899px) {
    .detecting {
        margin-top: 40px;
    }
    .detecting h3 {
        text-align: center;
        font-size: 25px;
    }
    .detecting h4 {
        font-size: 41px;
        font-weight: 400;
        color: #B3212D;
        text-align: center;
        margin: 30px auto; 
    }
    .detecting img {
        display: block;
        margin: 10px auto 30px;
    }
    .detecting-page .ism-button {
        background: #FBEF41;
    }
}
</style>
