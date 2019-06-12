<template>
    <div class="detection-page">
        <insightman-header-nav></insightman-header-nav>
        <div class="detection-tip">
            <h3>排廢檢測</h3>
            <div class="detection-tip-box">
                <h6>步驟一</h6>
                <p>將檢測儀導管置入排氣管</p>
            </div>
            <div class="detection-tip-box">
                <h6>步驟二</h6>
                <p>開啟檢測儀並坐在駕駛座</p>
            </div>
            <div class="detection-tip-box">
                <h6>步驟三</h6>
                <p>開啟藍芽後發動汽車</p>
            </div>
        </div>
        <router-link to="/connect" style="text-decoration: none;">
            <insightman-btn title="開始連線" bgColor="#FBEF41" bdColor="black"></insightman-btn>
        </router-link>
        <insightman-contact-us></insightman-contact-us>
    </div>
</template>

<script>
import InsightmanHeaderNav from '~/components/InsightmanHeaderNav.vue';
import InsightmanContactUs from '~/components/InsightmanContactUs.vue';
import InsightmanBtn from '~/components/InsightmanBtn.vue';
export default {
    components: {
        InsightmanHeaderNav,
        InsightmanContactUs,
        InsightmanBtn,
    }
}
</script>

<style>
@media (max-width:899px) {
    .detection-tip {
        margin-top: 40px; 
    }
    .detection-tip h3 {
        text-align: center;
        font-size: 25px;
    }
    .detection-tip-box {
        width: 80vw;
        height: 70px;
        margin: 40px auto;
    }
    .detection-tip-box h6 {
        display: block;
        font-size: 16px;
        color: white;
        background: #B3212D;
        text-align: center;
        padding: 5px;
        width: 90px;
        margin: auto;
        border-radius: 45px;
    }
    .detection-tip-box p {
        font-size: 20px;
        color: #B3212D;
        text-align: center;
        margin-top:15px; 
    }
}
</style>
