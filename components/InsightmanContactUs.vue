<template>
    <div class="ism-contactus">
        <img src="/line-2.png" alt="">
        <h3>{{$t('menu_contact')}}</h3>
        <p>{{$t('contact_text')}}</p>
        <form action="" method="post" class="ism-form">
            <div class="ism-form-each">
                <select name="question-type" required id="question-type">
                    <option value="select-quction">{{$t('contact_input_1')}}</option>
                    <option value="">{{$t('contact_input_1_option_1')}}</option>
                    <option value="">{{$t('contact_input_1_option_2')}}</option>
                    <option value="">{{$t('contact_input_1_option_3')}}</option>
                </select>
            </div>
            <div class="ism-form-each">
                <input type="text" name="guest-name" :placeholder="$t('contact_input_2')" required id="guest-name">
            </div>
            <div class="ism-form-each">
                <input type="text" name="guest-phone" :placeholder="$t('contact_input_3')" required id="guest-phone">
            </div>
            <div class="ism-form-each">
                <input type="text" name="guest-mail" :placeholder="$t('contact_input_4')" required id="guest-mail">
            </div>
            <div class="ism-form-each">
                <input type="text" name="guest-title" :placeholder="$t('contact_input_5')" required id="guest-title">
            </div>
            <div class="ism-form-each">
                <textarea type="text" name="guest-content" :placeholder="$t('contact_input_6')" required id="guest-content" rows="7">
                </textarea>
            </div>
            <insightman-btn :title="$t('all_btn_4')" bgColor="#FBEF41" bdColor="black" style="margin-bottom:20px;"></insightman-btn>
        </form>
        <img src="/line-3.png" alt="">
    </div>
</template>

<script>
import InsightmanLine from '~/components/InsightmanLine.vue';
import InsightmanBtn from '~/components/InsightmanBtn.vue';
export default {
    components:{
        InsightmanLine,
        InsightmanBtn,
    },
}
</script>

<style>
@media (max-width:899px) {
    #question-type {
        appearance:none;
    }
    .ism-contactus {
        position: relative;
        background-color: #B3212D;
        height: auto;
        width: 100vw;
        margin-top: 50px;
        padding-top: 50px; 
    }
    .ism-contactus img:first-child {
        position: absolute;
        margin-bottom: 30px;
        top: -3px;
        width: 100vw;
    }
    .ism-contactus img:last-child {
        margin-bottom: 0;
        width: 100vw;
    }
    .ism-contactus h3 {
        color: white;
        font-size: 22px;
        text-align: center;
    }
    .ism-contactus p {
        margin: 30px auto;
        width: 86vw;
        color: white;
        font-size: 16px;
    }
    .ism-form {
        width: 86vw;
        margin: 0 auto;
    }
    .ism-form-each {
        margin: 20px 0;
    }
    .ism-form-each input, .ism-form-each select {
        width: 100%;
        height: 45px;
        border: solid 3px #000;
        border-radius:0px; 
        padding-left: 10px ;
    }
    .ism-form-each select {
        z-index: 1;
        cursor: pointer;
        background: white;
    }
    .ism-form-each:first-child {
        position: relative;
    }
    .ism-form-each:first-child::after {
        position: absolute;
        content: '';
        top: 22px;
        right: 18px;
        transform: translateY(-75%) rotateZ(45deg);
        border-right: 3px solid;
        border-bottom: 3px solid;
        padding: 5px;
    }
    .ism-form-each textarea {
        width: 100%;
        border: solid 3px #000;
        padding-left: 10px 
    }
    .ism-form-each input::placeholder,.ism-form-each textarea::placeholder,.ism-form-each select  {
        color: #B3212D;
    }
    
}
</style>
