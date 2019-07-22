<template>
    <div>
        <h3 class="checkhold-title">排廢檢測</h3>
        <div class="findbase-title">
            <h4>尋找離您最近的服務保養中心</h4>
            <div class="ism-findbase-select">
                    <select name="question-type" required id="question-type" v-model="selected">
                        <option value="tainan">臺南市</option>
                        <option value="2">臺中市</option>
                        <option value="3">桃園市</option>
                        <option value="4">高雄市</option>
                    </select>
            </div>
            <p>將由專業人士為您檢驗汽車，全方位的保養服務包含：汽車美容、檢驗排氣、引擎維護、定期追蹤。</p>
            <!-- <insightman-btn title="立即搜尋" bgColor="#FBEF41" bdColor="black"></insightman-btn> -->
            <button class="ism-button" @click="$router.push('/findhold')">立即搜尋</button>
        </div>
    </div>
</template>

<script>
import InsightmanBtn from '~/components/InsightmanBtn.vue';
export default {
    layout: 'insightman',
    data:()=>({
        selected: 'tainan',
        holds: [],
    }),
    components: {
        InsightmanBtn,
    },
    async mounted(){
        if(process.client){
            this.holds = await require('~/config/insightman-stronghold')
        }
    },
    methods: {
        // findHold(){
        //     if(this.selected == 'tainan') {
        //         const array = this.holds.filter(hold => hold.tags.find(tag => tag == 'tainan'))
        //         const array_id = array.id
        //         this.$router.push('/findhold/'+array_id)
        //     }
        // }
    }
}
</script>

<style>
@media (max-width: 899px) {
    .findbase-title {
        margin-top: 30px; 
    }
    .findbase-title h4 {
        font-size: 22px;
        text-align: center;
        font-weight: 400;
    }
    .findbase-title p {
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
    .checkhold-title {
        text-align: center;
        margin-top: 30px;
        font-size: 25px;
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
