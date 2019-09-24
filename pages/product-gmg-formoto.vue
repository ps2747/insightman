<template>
    <div class="about-product-page">
        <h3 class="about-product-title">{{$t('all_btn_1')}}</h3>
        <insightman-product-info-for-gmg-moto :productDes="$t('index_product_des_3')" :productTitle="$t('index_product_3')" 
        :productLittltTitle="$t('gmgformoto_little_des')" productImg="/gmg-formoto.jpg" :infoTitle="$t('gmgformoto_1_title')" 
        :infoText="$t('gmgformoto_1_text')"
        ></insightman-product-info-for-gmg-moto>
        <insightman-product-gmg-for-moto-advantage></insightman-product-gmg-for-moto-advantage>
        <insightman-gmg-for-moto-knowledge></insightman-gmg-for-moto-knowledge>
        <insightman-line></insightman-line>
        <insightman-shop-link></insightman-shop-link>
    </div>
</template>

<script>
import InsightmanProductInfoForGmgMoto from '~/components/InsightmanProductInfoForGmgMoto.vue';
import InsightmanProductGmgForMotoAdvantage from '~/components/InsightmanProductGmgForMotoAdvantage.vue';
import InsightmanGmgForMotoKnowledge from '~/components/InsightmanGmgForMotoKnowledge.vue'
import InsightmanLine from '~/components/InsightmanLine.vue';
import InsightmanShopLink from '~/components/InsightmanShopLink.vue';
export default {
    layout: 'insightman',
    components: {
        InsightmanProductInfoForGmgMoto,
        InsightmanProductGmgForMotoAdvantage,
        InsightmanGmgForMotoKnowledge,
        InsightmanLine,
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