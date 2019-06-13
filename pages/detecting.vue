<template>
    <div class="detecting-page">
        <insightman-header-nav></insightman-header-nav>
        <div class="detecting" v-if="loading">
            <h3>進行檢測</h3>
            <h4>第一次靜態加速</h4>
            <img src="/detection/speedometer.png" alt="">
            <div class="detecting-progress">
                <progress-bar type="line" ref="line" :options="options"></progress-bar>
            </div>
        </div>
        <div class="detecting" v-if="!loading">
            <h3>進行檢測</h3>
            <h4>第二次靜態加速</h4>
            <img src="/detection/speedometer.png" alt="">
            <div class="detecting-progress">
                <progress-bar type="line" ref="second" :options="options"></progress-bar>
            </div>
        </div>
        <button class="ism-button" @click="oneMoreTime()" v-if="is_loading">下一步</button>
        <router-link to="/report" v-if="is_finish" style="text-decoration: none;">
            <insightman-btn title="檢測報告" bgColor="#FBEF41" bdColor="black"></insightman-btn>
        </router-link>
        <insightman-contact-us></insightman-contact-us>
    </div>
</template>

<script>
import Vue from 'vue';
import InsightmanHeaderNav from '~/components/InsightmanHeaderNav.vue';
import InsightmanContactUs from '~/components/InsightmanContactUs.vue';
import InsightmanBtn from '~/components/InsightmanBtn.vue';
import VueProgress from 'vue-progress'
Vue.use(VueProgress)

export default {
    data:()=>({
        loading: true,
        is_loading: false,
        is_finish: false,
        options: {
            color: '#B3212D',
            strokeWidth: 3,
            trailColor: '#f4f4f4',
            trailWidth: 3,
            duration: 6000,
            easing: 'easeOut',
            text: {
                className: 'progressbar__label',
                style: {
                    color: '#B3212D',
                    position: 'absolute',
                    right: '0px',
                    top: '10px',
                    padding: 0,
                    margin: 0,
                },
            },
            from: {color: '#FFEA82'},
            to: {color: '#ED6A5A'},
            step: (state, bar) => {
                bar.setText(Math.round(bar.value() * 100) + ' %')
            },
        }, 
    }),
    components: {
        InsightmanHeaderNav,
        InsightmanContactUs,
        InsightmanBtn,
    },
    methods:{
        async oneMoreTime(){
            this.$refs.line.animate(0)
            this.is_loading = false;
            this.loading = false;
            setTimeout(()=> {
                // this.loading = false;
                this.$refs.line.animate(1.0)
            }, 6000)
            setTimeout(()=> {
                this.is_finish = true;
            }, 12000)     
        },
    },
    mounted: function () {
        setTimeout(()=> {
            this.$refs.line.animate(1.0);
        },500)
        
        setTimeout(()=> {
            this.is_loading = true;
        },7000)
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
    .detecting-progress {
        width: 80vw;
        margin: 40px auto;
        position: relative;
    }
}
</style>
