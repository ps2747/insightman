<template>
    <div class="send-success">
        <h5>訊息發送成功</h5>
        <p>我們將立即為您處理，感謝您的耐心等候。</p>
        
        <!-- <insightman-btn title="商品介紹" bgColor="#FBEF41" bdColor="black"></insightman-btn> -->
        <button class="ism-button" @click="$router.push('/product')">商品介紹</button>
    </div>
</template>

<script>
import InsightmanBtn from '~/components/InsightmanBtn.vue';
export default {
    layout: 'insightman',
    components: {
        InsightmanBtn,
    }
}
</script>

<style>
@media (max-width: 899px) {
    .send-success h5 {
        text-align: center;
        font-size: 39px;
        font-weight: 300;
        margin-top: 50px;  
    }
    .send-success p {
        text-align: center;
        margin: 20px auto 50px; 
        font-size: 15px; 
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
