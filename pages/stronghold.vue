<template>
    <div>
        <div class="findbase-title">
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
            <button class="ism-button" @click="goContact">{{$t('all_btn_3')}}</button>
        </div>
        <div class="findbase-line"></div>
        <div class="findbase-select-area">
            <input type="radio" name="area" id="taiwan" value="1" v-model="select_area">
            <label class="findbase-select-taiwan" for="taiwan" @click="show_taiwan = true">{{$t('stronghold_tag_1')}}</label>
            <input type="radio" name="area" id="asia" value="2" v-model="select_area">
            <label class="findbase-select-asia" for="asia" @click="show_taiwan = false">{{$t('stronghold_tag_2')}}</label>
        </div>
        <div class="findbase-show-taiwan" v-if="select_area == '1'">
            <insightman-stronghold-block v-for="hold in getTaiwanHolds"
            :key="hold.id" :title="hold.title" :map="hold.map"
            :adress="hold.adress" :phone="hold.phone"></insightman-stronghold-block>
        </div>
        <div class="findbase-show-asia" v-if="select_area == '2'">
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
        select_area: '1',
    }),
    components: {
        InsightmanBtn,
        InsightmanStrongholdBlock
    },
    async mounted(){
        if(process.client){
            this.holds = await require('~/config/insightman-stronghold')

            if(sessionStorage['select_area']) {
                this.select_area = sessionStorage['select_area']
            }
        }
    },
    methods:{
        goContact(){
            if(this.$i18n.locale == 'CN') {
                this.$router.push('/CN/contact')
            } else {
                this.$router.push('/contact')
            }
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
        },
        getAsiaHolds(){
            if(this.holds) {
                const result_array = this.holds.filter(hold => hold.tags.find(tag => tag == 'asia'))
                return result_array;
            } else {
                return [];
            }
        },
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
        border-bottom: transparent solid 2px;
    }
    .findbase-select-area #taiwan:checked ~  .findbase-select-taiwan,
    .findbase-select-area #asia:checked ~ .findbase-select-asia {
        color: #000;
        border-bottom: #B3212D solid 2px;
    }
}
</style>
