<template>
  <div class="index-page">
    <div class="about-company-idea" style="margin-top:100px;position:relative;padding-top:80px;">
        <img src="/line-2.png" alt="">
        <img src="/insightman-index-logo.png" alt="" style="position:absolute;top: -50px;left: calc(50vw - 70px);width:140px;">
        <h3 style="text-align:left;padding-left:30px;">{{$t('index_1_title')}}</h3>
        <p v-html="$t('index_1_text')"></p>
        <img src="/line-4.png" alt="">
    </div>
    
    <insightman-front-product style="margin-top:80px;" :productDes="$t('index_product_des_1')" :productTitle="$t('index_product_1')" productImg="/engine-wizard.jpg" :goProduct="check_lang + '/product-engine-wizard'"></insightman-front-product>
    <insightman-front-product style="margin-top:80px;" :productDes="$t('index_product_des_2')" :productTitle="$t('index_product_2')" productImg="/gmg.jpg" :goProduct="check_lang + '/product-gmg'"></insightman-front-product>
    <insightman-front-product style="margin-top:80px;" :productDes="$t('index_product_des_3')" :productTitle="$t('index_product_3')" productImg="/gmg-formoto.jpg" :goProduct="check_lang + '/product-gmg-formoto'"></insightman-front-product>
      <!-- <insightman-btn title="產品介紹" bgColor="#FBEF41" bdColor="black"></insightman-btn> -->
      
    <insightman-line></insightman-line>
    <div class="index-block">
      <h4 class="index-title">{{$t('index_2_title')}}</h4>
      <img style="width: 70%;margin: 50px auto; display: block;" src="/engine-wizard-logo.png" alt="">
      <p v-html="$t('index_2_text')"></p>
      <button class="ism-button red-button" style="margin-top: 50px;" @click="goEW">{{$t('all_btn_2')}}</button>
      <!-- <insightman-feature-block src="/feature/feature-01.png" title="節能" content="爆發力瞬間增加<br>35%減少油耗、續航力大增"></insightman-feature-block>
      <insightman-feature-block src="/feature/feature-02.png" title="環保" content="提升引擎運轉效率<br>立竿見影、降低廢氣排放"></insightman-feature-block>
      <insightman-feature-block src="/feature/feature-03.png" title="減碳" content="化解油阻，磨擦，油門輕勁<br>活化機油、不會沈積油泥"></insightman-feature-block>
      <insightman-feature-block src="/feature/feature-04.png" title="節費" content="保護引擎，延緩機件磨損<br>延長使用壽命，節省維修費用"></insightman-feature-block> -->
    </div>
    <insightman-line></insightman-line>
    <insightman-shop-link></insightman-shop-link>
    <insightman-line></insightman-line>
    
    <insightman-find-base></insightman-find-base>
  </div>
</template>

<script>
import InsightmanFrontProduct from '~/components/InsightmanFrontProduct.vue';
import InsightmanBtn from '~/components/InsightmanBtn.vue';
import InsightmanLine from '~/components/InsightmanLine.vue';
import InsightmanFeatureBlock from '~/components/InsightmanFeatureBlock.vue';
import InsightmanShopLink from '~/components/InsightmanShopLink.vue';
import InsightmanFindBase from '~/components/InsightmanFindBase.vue';
export default {
  layout:'insightman',
  data:()=>({
    check_lang: '',
  }),
  mounted(){
    if(process.client) {
      if(this.$i18n.locale == 'CN') {
        this.check_lang = '/CN'
      } else {
        this.check_lang = ''
      }
    }
  },
  components: {
    InsightmanBtn,
    InsightmanFrontProduct,
    InsightmanLine,
    InsightmanFeatureBlock,
    InsightmanShopLink,
    InsightmanFindBase,
  },
  methods: {
    goEW(){
      window.location.href = 'http://tw.enginewizard.co.uk/'
    }
  }
}
</script>

<style>
@media (max-width: 899px) {
  .index-page {
    width: 100vw;
  }
  .index-title {
    font-size: 25px;
    font-weight: 500;  
    text-align: center;
  }
  li a {
    text-decoration: none;
  }
  .index-block p{
    width: 86vw;
    margin: 0 auto;
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
  .red-button {
    background-color: #B3212D !important;
    color: #fff !important;
    border: 3px solid #000 !important;
  }

  .about-company-idea {
        position: relative;
        background-color: #B3212D;
        height: auto;
        width: 100vw;
        margin-top: 50px;
        padding-top: 50px; 
    }
    .about-company-idea img:first-child {
        position: absolute;
        margin-bottom: 30px;
        top: -3px;
        width: 100vw;
    }
    .about-company-idea img:last-child {
        margin-bottom: -30px;
        width: 100vw;
    }
    .about-company-idea h3 {
        color: white;
        font-size: 22px;
        text-align: center;
    }
    .about-company-idea p {
        margin: 30px auto;
        width: 86vw;
        color: white;
        font-size: 16px;
    }
}
</style>
