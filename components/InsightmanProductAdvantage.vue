<template>
    <div class="ism-product-advantage">
        <!-- <img src="/product/background-line-1.png" alt=""> -->
        <div class="product-advantage-content">
            <h4 style="text-align: center;">{{$t('engine_2_title')}}</h4>
            <img style="width: 100%;" src="/engine-wizard-fea.jpg" alt="">
            <h5>{{$t('engine_2_little_title_1')}}</h5>
            <p v-html="$t('engine_2_text_1')"></p>
            <h5>{{$t('engine_2_little_title_2')}}</h5>
            <p v-html="$t('engine_2_text_2')"></p>
            <h5>{{$t('engine_2_little_title_3')}}</h5>
            <p v-html="$t('engine_2_text_3')"></p>
            <h5>{{$t('engine_2_little_title_4')}}</h5>
            <p v-html="$t('engine_2_text_4')"></p>
        </div>
        <img src="/line-6.png" alt="">
    </div>
</template>

<script>
export default {

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
}
</style>
