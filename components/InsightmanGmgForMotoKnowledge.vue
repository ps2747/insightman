<template>
    <div class="ism-market-research">
        <div class="market-text-data-formoto" id="text-data-area-3">
            <h4 style="text-align: center;">{{$t('gmgformoto_3_title_1')}}</h4>
            <h6 style="text-align: center;font-size: 20px;">{{$t('gmgformoto_3_little_title')}}</h6>
            <p v-html="$t('gmgformoto_3_text_1')"></p>
            <h4 style="text-align: center;">{{$t('gmgformoto_3_title_2')}}</h4>
            <p v-html="$t('gmgformoto_3_text_2')"></p>
        </div>
        <img style="width:100%;" src="/gmg-formoto.jpg" alt="">
        <div class="market-text-data-formoto">
            <h4>{{$t('gmgformoto_4_title_1')}}</h4>
            <p v-html="$t('gmgformoto_4_text_1')"></p>
            <h4 v-html="$t('gmgformoto_4_title_2')"></h4>
            <p v-html="$t('gmgformoto_4_text_2')"></p>
        </div>
        <insightman-line></insightman-line>
        <div class="market-text-data-formoto">
            <h4>{{$t('gmgformoto_5_title')}}</h4>
            <p v-html="$t('gmgformoto_5_text')"></p>
        </div>
    </div>
</template>

<script>
import InsightmanLine from '~/components/InsightmanLine.vue'
export default {
    components:{
        InsightmanLine,
    }
}
</script>

<style>
@media (max-width: 899px) {
    .ism-market-research {
        margin-top: 70px; 
        position: relative;
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
    .market-text-data-formoto {
        width: 86%;
        /* height: 300px;
        overflow: hidden; */
        margin: 0 auto;
        position: relative; 
        /* background: linear-gradient(180deg,rgb(255, 255, 255) 15%, rgba(255, 255, 255, 0) 100%); */
    }
    .long-style {
        height: auto;
    }
    .market-text-data-formoto p {
        font-size: 20px;
    }
    .market-text-data-formoto h4 {
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