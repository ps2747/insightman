<template>
    <div class="about-product-page">
        <insightman-header-nav></insightman-header-nav>
        <h3 class="about-product-title">商品介紹</h3>
        <insightman-front-product style="margin-top:40px;"></insightman-front-product>
        <insightman-btn title="線上商城" bgColor="#FBEF41" bdColor="black"></insightman-btn>
        <insightman-product-advantage></insightman-product-advantage>
        <insightman-market-research></insightman-market-research>
        <insightman-contact-us></insightman-contact-us>
    </div>
</template>

<script>
import InsightmanHeaderNav from '~/components/InsightmanHeaderNav.vue';
import InsightmanFrontProduct from '~/components/InsightmanFrontProduct.vue';
import InsightmanBtn from '~/components/InsightmanBtn.vue';
import InsightmanProductAdvantage from '~/components/InsightmanProductAdvantage.vue';
import InsightmanMarketResearch from '~/components/InsightmanMarketResearch.vue';
import InsightmanContactUs from '~/components/InsightmanContactUs.vue';
export default {
    components:{
        InsightmanHeaderNav,
        InsightmanFrontProduct,
        InsightmanBtn,
        InsightmanProductAdvantage,
        InsightmanMarketResearch,
        InsightmanContactUs,
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
}
</style>
