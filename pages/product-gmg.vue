<template>
    <div class="about-product-page">
        <h3 class="about-product-title">{{$t('all_btn_1')}}</h3>
        <insightman-product-info :productDes="$t('index_product_des_2')" :productTitle="$t('index_product_2')" 
        productImg="/gmg.jpg" :infoTitle="$t('gmg_1_title')"
        :infoText="$t('gmg_1_text')"></insightman-product-info>
        <insightman-product-gmg-advantage></insightman-product-gmg-advantage>
        <insightman-gmg-knowledge></insightman-gmg-knowledge>
        <insightman-line></insightman-line>
        <insightman-shop-link></insightman-shop-link>
    </div>
</template>

<script>
import InsightmanProductInfo from '~/components/InsightmanProductInfo.vue';
import InsightmanProductGmgAdvantage from '~/components/InsightmanProductGmgAdvantage.vue';
import InsightmanLine from '~/components/InsightmanLine.vue';
import InsightmanGmgKnowledge from '~/components/InsightmanGmgKnowledge.vue';
import InsightmanShopLink from '~/components/InsightmanShopLink.vue';
export default {
    layout: 'insightman',
    components: {
        InsightmanProductInfo,
        InsightmanProductGmgAdvantage,
        InsightmanLine,
        InsightmanGmgKnowledge,
        InsightmanShopLink,
    }
}
</script>

<style>
@media (max-width: 899px) {
    .about-product-title {
        text-align: center;
        margin-top: 30px;
        font-size: 25px;
    }
}
</style>