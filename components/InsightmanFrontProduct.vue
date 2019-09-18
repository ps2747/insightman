<template>
    <div class="front-product">
        <h6>{{productDes}}</h6>
        <h2>{{productTitle}}</h2>
        <div class="front-product-box">
            <img :src="productImg" alt="">
        </div>
        <button class="ism-button" @click="$router.push(goProduct)">{{$t('all_btn_1')}}</button>
    </div>
</template>

<script>
export default {
    props: {
        productDes: String,
        productTitle: String,
        productImg: String,
        goProduct: String,
    }
}
</script>

<style>
@media (max-width: 899px) {
    .front-product {
        text-align: center;
    }
    .front-product h6 {
        font-size: 19px;
        font-weight: 300;
        margin-top: 30px;
    }
    .front-product h2 {
        font-size: 59px;
        font-weight: 300;
        margin-top: 10px;  
    }
    .front-product-box {
        margin: 35px auto;
    }
    .front-product-box img {
        width: 100%;
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
