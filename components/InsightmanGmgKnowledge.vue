<template>
    <div class="ism-market-research">
        <div class="market-text-data" id="text-data-area-3">
            <h4>{{$t('gmg_3_title')}}</h4>
            <p v-html="$t('gmg_3_text')"></p>
        </div>
        <button style="background-color:#FBEF41;border-color:#000;margin-top:20px;" v-if="!open_more" class="ism-button" @click="readMore">{{$t('all_btn_5')}}</button>
    </div>
</template>

<script>
export default {
    data:()=>({
        open_more: false,
    }),
    methods: {
        readMore(){
            document.getElementById('text-data-area-3').classList.add('long-style')
            this.open_more = true
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
    .long-style {
        height: auto;
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