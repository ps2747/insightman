<template>
    <div class="product-info">
        <h6>{{productDes}}</h6>
        <h2>{{productTitle}}</h2>
        <div class="front-product-box">
            <img :src="productImg" alt="">
        </div>
        <div class="product-info-text">
            <div class="product-info-text-data">
                <h4>{{infoTitle}}</h4>
                <p v-html="infoText"></p>
            </div>
        </div>
        <img style="width: 100%;position: absolute; left: 0;z-index:999;" src="/line-4.png" alt="">
    </div>
</template>

<script>
export default {
    props: {
        productDes: String,
        productTitle: String,
        productImg: String,
        infoTitle: String,
        infoText: String,
    }
}
</script>

<style>
@media (max-width: 899px) {
    .product-info {
        text-align: center;
        margin-top: 30px;
        font-size: 25px;
        position: relative;
    }
    .product-info h6 {
        font-size: 19px;
        font-weight: 300;
        margin-top: 30px;
    }
    .product-info h2 {
        font-size: 59px;
        font-weight: 300;
        margin-top: 10px;  
    }
    .product-info .front-product-box {
        margin: 35px auto 0;
    }
    .product-info .front-product-box img {
        width: 100%;
    }
    .product-info-text {
        background: #B3212D;
        text-align: left;
        padding-top: 30px;
        padding-bottom: 25px;
        color: #fff;
    }
    .product-info-text-data {
        width: 86%;
        margin: 0 auto;
    }
    .product-info-text h4 {
        font-size: 29px;
        line-height: 40px;
        margin-top: 0;
    }
    .product-info-text p {
        font-size: 20px;
    }
}
</style>