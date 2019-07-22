<template>
    <div>
        <div class="findbase-title">
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
            <!-- <insightman-btn title="立即預約" bgColor="#FBEF41" bdColor="black"></insightman-btn> -->
            <button class="ism-button" @click="$router.push('/sendsuccess')">立即預約</button>
        </div>
        <div class="findbase-line"></div>
        <div class="findbase-select-area">
            <input type="radio" name="area" id="taiwan" checked>
            <label class="findbase-select-taiwan" for="taiwan" @click="show_taiwan = true">臺灣地區</label>
            <input type="radio" name="area" id="asia">
            <label class="findbase-select-asia" for="asia" @click="show_taiwan = false">亞太地區</label>
        </div>
        <div class="findbase-show-taiwan" v-if="show_taiwan">
            <insightman-stronghold-block v-for="hold in getTaiwanHolds"
            :key="hold.id" :title="hold.title" :map="hold.map"
            :adress="hold.adress" :phone="hold.phone"></insightman-stronghold-block>
        </div>
        <div class="findbase-show-asia" v-if="!show_taiwan">
            <insightman-stronghold-block v-for="hold in getAsiaHolds"
            :key="hold.id" :title="hold.title" :map="hold.map"
            :adress="hold.adress" :phone="hold.phone"></insightman-stronghold-block>
        </div>
    </div>
</template>

<script>
import InsightmanBtn from '~/components/InsightmanBtn.vue';
import InsightmanStrongholdBlock from '~/components/InsightmanStrongholdBlock.vue';
export default {
    layout: 'insightman',
    data:()=>({
        holds: [],
        show_taiwan:true,
    }),
    components: {
        InsightmanBtn,
        InsightmanStrongholdBlock
    },
    async mounted(){
        if(process.client){
            this.holds = await require('~/config/insightman-stronghold')
        }
    },
    computed:{
        getTaiwanHolds(){
            if(this.holds) {
                const result_array = this.holds.filter(hold => hold.tags.find(tag => tag == 'taiwan'))
                return result_array;
            } else {
                return [];
            }
        },getAsiaHolds(){
            if(this.holds) {
                const result_array = this.holds.filter(hold => hold.tags.find(tag => tag == 'asia'))
                return result_array;
            } else {
                return [];
            }
        }
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
    .findbase-line {
        background: #000;
        width: 15vw;
        height: 1vh;
        border-radius: 50px;
        margin: 40px auto;
    }
    .findbase-select-area {
        display: flex;
        align-items: center;
        justify-content: space-evenly;
    }
    .findbase-select-area input {
        display: none;
    }
    .findbase-select-area label {
        color: #ACACAC;
        font-size: 21px;
        font-weight: 500;
        border-bottom: #FFF solid 2px;
    }
    .findbase-select-area #taiwan:checked ~  .findbase-select-taiwan,
    .findbase-select-area #asia:checked ~ .findbase-select-asia {
        color: #000;
        border-bottom: #B3212D solid 2px;
    }
}
</style>
