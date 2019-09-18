<template>
    <div>
        <h4 class="index-title">{{$t('all_link_title')}}</h4>
        <div class="shop-link-icon">
            <img src="/shopee-icon.png" alt="">
            <img src="/ruten-icon.png" alt="">
            <img src="/pchome-icon.png" alt="">
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>
@media (max-width: 899px) {
    .index-title {
        font-size: 25px;
        font-weight: 500;  
        text-align: center;
    }
    .shop-link-icon img {
        display: block;
        margin: 60px auto;
    }
    .shop-link-icon img:first-child,
    .shop-link-icon img:nth-child(2) {
        width: 20%;
    }
    .shop-link-icon img:last-child {
        width: 40%;
    }
}
</style>