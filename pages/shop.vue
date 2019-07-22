<template>
    <div>
        <h3 class="shop-title">線上商城</h3>
        <div class="ism-findbase-select">
            <select name="question-type" required id="question-type">
                <option value="select-tainan">商品名稱</option>
                <option value="select-taichung">商品名稱</option>
                <option value="select-taoyuan">商品名稱</option>
                <option value="select-kaohsiung">商品名稱</option>
            </select>
        </div>
        <insightman-product-preview v-for="product in products"
        :key="product.id" :title="product.title" :img="product.picture"
        ></insightman-product-preview>
    </div>
</template>

<script>
import InsightmanProductPreview from '~/components/InsightmanProductPreview.vue';
export default {
    layout: 'insightman',
    data:()=>({
        products: []
    }),
    components:{
        InsightmanProductPreview,
    },
    async mounted(){
        if(process.client){
            this.products = await require('~/config/insightman-product')
        }
    }
}
</script>

<style>
@media (max-width: 899px) {
    .shop-title {
        text-align: center;
        margin-top: 30px;
        font-size: 25px;
    }
    .ism-findbase-select {
        position: relative;
        width: 86vw;
        margin: 15px auto;
    }
    .ism-findbase-select::after {
        position: absolute;
        content: '';
        top: 25px;
        right: 18px;
        transform: translateY(-75%) rotateZ(45deg);
        border-right: 3px solid;
        border-bottom: 3px solid;
        padding: 5px;
    }
    .ism-findbase-select select {
        color: #B3212D;
        width: 100%;
        height: 50px;
        border: solid 3px #000;
        border-radius:0px; 
        padding-left: 10px ;
        font-size: 22px;
        background: white;
    }
}
</style>
