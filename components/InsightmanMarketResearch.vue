<template>
    <div class="ism-market-research">
        <div class="ism-market-research-title">
            <h3>市場數據報告</h3>
            <h5>引擎精靈已超過10萬輛汽車使用</h5>
        </div>
        <div class="ism-market-research-box">
            <h6>「CO」降低幅度</h6>
            <img src="/product/market-1.png" alt="">
        </div>
        <div class="ism-market-research-box">
            <h6>「HC」降低幅度</h6>
            <img src="/product/market-2.png" alt="">
        </div>
        <div class="ism-market-research-box">
            <h6>節省油耗比例</h6>
            <img src="/product/market-3.png" alt="">
        </div>
        <div class="ism-market-research-box">
            <h6>引擎爆發力增加</h6>
            <img src="/product/market-4.png" alt="">
        </div>
        <insightman-btn title="更多產品" bgColor="#FBEF41" bdColor="black"></insightman-btn>
    </div>
</template>

<script>
import InsightmanBtn from '~/components/InsightmanBtn.vue';
export default {
    components: {
        InsightmanBtn,
    }
}
</script>

<style>
@media (max-width: 899px) {
    .ism-market-research {
        margin-top: 70px; 
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
}
</style>
