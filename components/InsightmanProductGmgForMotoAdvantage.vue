<template>
    <div class="ism-product-advantage">
        <!-- <img src="/product/background-line-1.png" alt=""> -->
        <div class="product-advantage-content">
            <h4>{{$t('gmgformoto_2_title')}}</h4>
            <img style="width: 100%;" src="/gmgformoto-fea.jpg" alt="">
            <div id="text-area" style="margin-top:20px;">
                <p v-html="$t('gmgformoto_2_text')"></p>
            </div>
        </div>
        <img src="/line-6.png" alt="">
    </div>
</template>

<script>
export default {
    data:()=>({
        
    }),
    methods: {
        
    }
    
}
</script>

<style>
@media (max-width: 899px) {
    .ism-product-advantage {
        position: relative;
        background: #FBEF41;
        height: auto;
        /* margin-top: 70px;  */
        padding-top:30px; 
        padding-bottom: 20px;
    }
    .ism-product-advantage img:first-child {
        position: absolute;
        width: 100vw;
        top: -4.9vh;
    }
    .product-advantage-content {
        /* background: red; */
        width: 86vw;
        height: auto;
        margin: 30px auto;
    }
    .product-advantage-content h4 {
        font-size: 29px;
        line-height: 40px;
        margin-top: 30px;
    }
    .product-advantage-content h5 {
        font-size: 24px;
        line-height: 40px;
        margin-top: 30px;
        margin-bottom: 0px;
    }
    .product-advantage-content p {
        margin-top: 5px;
        font-size: 20px;
    } 
    .ism-product-advantage img:last-child {
        position: absolute;
        width: 100vw;
        bottom: -4.1vh;
    }
    .short-style {
        height: 300px;
        overflow: hidden;
    }
    .long-style {
        height: auto;
    }
}
</style>