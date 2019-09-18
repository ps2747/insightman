<template>
    <div class="about-product-page">
        <h3 class="about-product-title">{{$t('all_btn_1')}}</h3>
        <insightman-product-info :productDes="$t('index_product_des_1')" :productTitle="$t('index_product_1')" 
        productImg="/engine-wizard.jpg" :infoTitle="$t('engine_1_title')"
        :infoText="$t('engine_1_text')"></insightman-product-info>
        
        <insightman-product-advantage></insightman-product-advantage>
        <insightman-market-research></insightman-market-research>
        <insightman-line></insightman-line>
        <insightman-shop-link></insightman-shop-link>
    </div>
</template>

<script>
import InsightmanProductInfo from '~/components/InsightmanProductInfo.vue';
// import InsightmanFrontProduct from '~/components/InsightmanFrontProduct.vue';
import InsightmanBtn from '~/components/InsightmanBtn.vue';
import InsightmanProductAdvantage from '~/components/InsightmanProductAdvantage.vue';
import InsightmanMarketResearch from '~/components/InsightmanMarketResearch.vue';
import InsightmanLine from '~/components/InsightmanLine.vue';
import InsightmanShopLink from '~/components/InsightmanShopLink.vue';
export default {
    layout: 'insightman',
    components:{
        InsightmanProductInfo,
        // InsightmanFrontProduct,
        InsightmanBtn,
        InsightmanProductAdvantage,
        InsightmanMarketResearch,
        InsightmanLine,
        InsightmanShopLink,
    },
}
</script>

<style>
@media (max-width:899px) {
    .about-product-title {
        text-align: center;
        margin-top: 30px;
        font-size: 25px;
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
        background-color: #FBEF41; 
        color: black;
        cursor: pointer;
    }
}
</style>
