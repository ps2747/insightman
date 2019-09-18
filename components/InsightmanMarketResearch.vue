<template>
    <div class="ism-market-research">
        <div class="ism-market-research-title">
            <h3>{{$t('engine_3_title')}}</h3>
            <h5>{{$t('engine_3_little_title')}}</h5>
        </div>
        <div class="ism-market-research-box">
            <h6>{{$t('engine_3_block_1')}}</h6>
            <img src="/product/market-1.png" alt="">
        </div>
        <div class="ism-market-research-box">
            <h6>{{$t('engine_3_block_2')}}</h6>
            <img src="/product/market-2.png" alt="">
        </div>
        <div class="ism-market-research-box">
            <h6>{{$t('engine_3_block_3')}}</h6>
            <img src="/product/market-3.png" alt="">
        </div>
        <div class="ism-market-research-box">
            <h6>{{$t('engine_3_block_4')}}</h6>
            <img src="/product/market-4.png" alt="">
        </div>
        <div class="market-text-data" id="text_data_area">
            <p v-html="$t('engine_3_text_1')"></p>
            <h4>{{$t('engine_3_little_title_1')}}</h4>
            <p v-html="$t('engine_3_little_text_1')"></p>
            <h4>{{$t('engine_3_little_title_2')}}</h4>
            <p v-html="$t('engine_3_little_text_2')"></p>
            <h4>{{$t('engine_3_little_title_3')}}</h4>
            <p v-html="$t('engine_3_little_text_3')"></p>
        </div>
        <button style="background-color:#FBEF41;border-color:#000" v-if="!open_more" class="ism-button" @click="readMore">{{$t('all_btn_5')}}</button>
        <insightman-line></insightman-line>
        <div class="market-text-data" id="text-data-area-2">
            <h4 style="font-size:25px;margin-top:50px;">{{$t('engine_4_title')}}</h4>
            <p v-html="$t('engine_4_text')"></p>
        </div>
        <button style="background-color:#FBEF41;border-color:#000;margin-top:15px;" v-if="!open_more_2" class="ism-button" @click="readMore2">{{$t('all_btn_5')}}</button>
        <!-- <insightman-btn title="更多產品" bgColor="#FBEF41" bdColor="black"></insightman-btn> -->
    </div>
</template>

<script>
import InsightmanLine from '~/components/InsightmanLine.vue';
import InsightmanBtn from '~/components/InsightmanBtn.vue';
export default {
    data:()=>({
        open_more: false,
        open_more_2: false,
    }),
    components: {
        InsightmanBtn,
        InsightmanLine,
    },
    methods:{
        readMore(){
            document.getElementById('text_data_area').style.height = 'auto';
            this.open_more = true;
        },
        readMore2(){
            document.getElementById('text-data-area-2').style.height = 'auto';
            this.open_more_2 = true
        }
    }
}
</script>

<style>
@media (max-width: 899px) {
    .ism-market-research {
        margin-top: 70px; 
        position: relative;
    }
    .ism-market-research-title h3 {
        font-size: 29px;
        font-weight: bold;
        text-align: center;
    }
    .ism-market-research-title h5 {
        font-size: 20px;
        text-align: center;
        font-weight: 400;
    }
    .ism-market-research-box {
        width: 50vw;
        margin: 70px auto;
    }
    .ism-market-research-box h6 {
        font-size: 20px;
        font-weight: 400;
        text-align: center;
        border-bottom: 2px solid #B3212D;
        padding-bottom: 15px;        
    }
    .ism-market-research-box img {
        display: block;
        margin: 15px auto 0;
        width: 35vw;
    }
    .market-text-data {
        width: 86%;
        height: 300px;
        overflow: hidden;
        margin: 0 auto;
        position: relative; 
        /* background: linear-gradient(180deg,rgb(255, 255, 255) 15%, rgba(255, 255, 255, 0) 100%); */
    }
    .market-text-data p {
        font-size: 17px;
    }
    .market-text-data h4 {
        font-size: 29px;
        line-height: 40px;
        margin-top: 30px;
    }
    .ism-button {
        width: 150px;
        height: 50px;
        border: solid;
        border-radius: 25px;
        display: block;
        margin: auto;
        font-size: 21px;
        font-weight: bold;
    }
}
</style>
