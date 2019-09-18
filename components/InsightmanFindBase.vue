<template>
    <div class="ism-findbase">
        <img src="/find/findBase-logo.png" alt="">
        <img src="/find/findBase-picture.png" alt="">
        <h4>{{$t('reservation_title')}}</h4>
        <div class="ism-findbase-select">
                <select name="question-type" required id="question-type">
                    <option value="select-tainan">{{$t('reservation_option_1')}}</option>
                    <option value="select-taichung">{{$t('reservation_option_2')}}</option>
                    <option value="select-taoyuan">{{$t('reservation_option_3')}}</option>
                    <option value="select-kaohsiung">{{$t('reservation_option_4')}}</option>
                </select>
        </div>
        <p>{{$t('reservation_text')}}</p>
        <!-- <insightman-btn title="立即預約" bgColor="#FBEF41" bdColor="black"></insightman-btn> -->
        <button style="background-color:#FBEF41;border-color:#000;margin-top:15px;" @click="goContact" class="ism-button">{{$t('all_btn_3')}}</button>
    </div>
</template>

<script>
import InsightmanBtn from '~/components/InsightmanBtn.vue';
export default {
    components:{
        InsightmanBtn,
    },
    methods: {
        goContact(){
            if(this.$i18n.locale == 'CN') {
                this.$router.push('/CN/contact')
            } else {
                this.$router.push('/contact')
            }
        }
    }
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
    .ism-button {
        width: 150px;
        height: 50px;
        border: solid;
        border-radius: 25px;
        display: block;
        margin: auto;
        font-size: 21px;
        font-weight: bold;
    }
}
</style>
