<template>
    <div class="product-block-border">
        <div class="product-block">
            <div class="product-block-title">{{title}}</div>
            <img :src="'/'+img+'.png'" alt="">
        </div>
        <button class="ism-button">商品介紹</button>
    </div>
</template>

<script>
import InsightmanBtn from '~/components/InsightmanBtn.vue'
export default {
    props: {
        title: String,
        img: String,
    },
    components: {
        InsightmanBtn,
    }
}
</script>

<style>
@media (max-width: 899px) {
    .product-block-border {
        margin-top: 50px;
    }
    .product-block {
        width: 95vw;
        height: auto;
        border: 5px #000 solid;
        margin: 10px auto;
    }
    .product-block-title {
        background-color:#B3212D;
        color: #fff; 
        display: flex;
        align-items: center;
        justify-content: center;
        height: 35px;
        font-size: 17px; 
    }
    .product-block img {
        display: block;
        margin: 30px auto;
        height: 250px;
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
