<template>
    <div class="stronghold-block">
        <div class="stronghold-block-title">{{title}}</div>
        <iframe :src="map" width="100%" height="300" frameborder="0" style="border:0" allowfullscreen></iframe>
        <div class="stronghold-block-data">
            <div class="stronghold-block-data-li">
                <img src="/stronghold/adress-icon.png" alt="">
                <p v-html="adress"></p>
            </div>
            <div class="stronghold-block-data-li">
                <img src="/stronghold/phone-icon.png" alt="">
                <p v-html="phone"></p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props:{
        title: String,
        map: String,
        adress: String,
        phone: String,
    }
}
</script>

<style>
@media (max-width: 899px) {
    .stronghold-block {
        width: 95vw;
        height: auto;
        border: 5px #000 solid;
        margin: 10px auto;
    }
    .stronghold-block-title {
        background-color:#B3212D;
        color: #fff; 
        display: flex;
        align-items: center;
        justify-content: center;
        height: 35px;
        font-size: 17px; 
    }
    .stronghold-block-data {
        padding-left: 5vw; 
        min-height: 80px;
        margin-top: 5px;
    }
    .stronghold-block-data-li {
        display: flex;
        align-items: flex-start;
        min-height: 40px;
        margin-top: 5px;
    }
    .stronghold-block-data-li img {
        margin-right: 5px; 
    }
    .stronghold-block-data-li p {
        font-size: 13px;
        margin: 0;
        width: 85%;
    }
}
</style>
