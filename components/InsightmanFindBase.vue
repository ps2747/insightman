<template>
    <div class="ism-findbase">
        <img src="/findBase/findBase-logo.png" alt="">
        <img src="/findBase/findBase-picture.png" alt="">
        <h4>尋找離您最近的服務保養中心</h4>
        <div class="ism-findbase-select">
                <select name="question-type" required id="question-type">
                    <option value="select-tainan">臺南市</option>
                    <option value="select-taichung">臺中市</option>
                    <option value="select-taoyuan">桃園市</option>
                    <option value="select-kaohsiung">高雄市</option>
                </select>
        </div>
        <p>將由專業人士為您檢驗汽車，全方位的保養服務包含：汽車美容、檢驗排氣、引擎維護、定期追蹤。</p>
        <insightman-btn title="立即預約" bgColor="#FBEF41" bdColor="black"></insightman-btn>
    </div>
</template>

<script>
import InsightmanBtn from '~/components/InsightmanBtn.vue';
export default {
    components:{
        InsightmanBtn,
    },
}
</script>

<style>
@media (max-width: 899px) {
    .ism-findbase img {
        display: block;
        margin: 25px auto;
    }
    .ism-findbase img:nth-child(2) {
        width: 100vw;
    }
    .ism-findbase h4 {
        font-size: 22px;
        text-align: center;
        font-weight: 400;
    }
    .ism-findbase p {
        width: 83vw;
        margin: auto;
        font-size: 14px;
        margin: 30px auto; 
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
