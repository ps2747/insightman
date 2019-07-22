<template>
  <div class="index-page">
    <!-- <insightman-header-nav></insightman-header-nav> -->
    <insightman-front-product></insightman-front-product>
      <!-- <insightman-btn title="產品介紹" bgColor="#FBEF41" bdColor="black"></insightman-btn> -->
      <button class="ism-button" @click="$router.push('/product')">產品介紹</button>
    <insightman-line></insightman-line>
    <div class="index-block">
      <h4 class="index-title">四大特色</h4>
      <insightman-feature-block src="/feature/feature-01.png" title="節能" content="爆發力瞬間增加<br>35%減少油耗、續航力大增"></insightman-feature-block>
      <insightman-feature-block src="/feature/feature-02.png" title="環保" content="提升引擎運轉效率<br>立竿見影、降低廢氣排放"></insightman-feature-block>
      <insightman-feature-block src="/feature/feature-03.png" title="減碳" content="化解油阻，磨擦，油門輕勁<br>活化機油、不會沈積油泥"></insightman-feature-block>
      <insightman-feature-block src="/feature/feature-04.png" title="節費" content="保護引擎，延緩機件磨損<br>延長使用壽命，節省維修費用"></insightman-feature-block>
    </div>
    <insightman-line></insightman-line>
    <insightman-find-base></insightman-find-base>
    <!-- <insightman-contact-us></insightman-contact-us> -->
  </div>
</template>

<script>
// import InsightmanHeaderNav from '~/components/InsightmanHeaderNav.vue';
import InsightmanFrontProduct from '~/components/InsightmanFrontProduct.vue';
import InsightmanBtn from '~/components/InsightmanBtn.vue';
import InsightmanLine from '~/components/InsightmanLine.vue';
import InsightmanFeatureBlock from '~/components/InsightmanFeatureBlock.vue';
import InsightmanFindBase from '~/components/InsightmanFindBase.vue';
// import InsightmanContactUs from '~/components/InsightmanContactUs.vue';
export default {
  layout:'insightman',
  components: {
    // InsightmanHeaderNav,
    InsightmanBtn,
    InsightmanFrontProduct,
    InsightmanLine,
    InsightmanFeatureBlock,
    InsightmanFindBase,
    // InsightmanContactUs,
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
