<template>
    <div class="Report-detection-page">
        <insightman-header-nav></insightman-header-nav>
        <div class="Report-detection">
            <h3>檢測報告</h3>
            <div class="Report-content">
                <div class="Report-content-li" v-for="(value,name) in report" :key="name">
                    <h4>{{name}}</h4>
                    <p v-if="value=='正常值'">{{value}}</p>
                    <p style="color:#B3212D" v-else>{{value}}</p>
                </div>
                <!-- <div class="Report-content-li">
                    <h4>HC</h4>
                    <p style="color:#B3212D">超標</p>
                </div>
                <div class="Report-content-li">
                    <h4>CO2</h4>
                    <p>正常值</p>
                </div> -->
            </div>
        </div>
        <router-link to="/member" style="text-decoration: none;">
            <insightman-btn title="會員中心" bgColor="#FBEF41" bdColor="black"></insightman-btn>
        </router-link>
        <insightman-contact-us></insightman-contact-us>
    </div>
</template>

<script>
import InsightmanHeaderNav from '~/components/InsightmanHeaderNav.vue';
import InsightmanContactUs from '~/components/InsightmanContactUs.vue';
import InsightmanBtn from '~/components/InsightmanBtn.vue';


export default {
    data:()=> ({
        report: {
            CO: '正常值',
            HC: '超標',
            CO2: '正常值',
        },
        // isActive: false,
    }),
    components: {
        InsightmanHeaderNav,
        InsightmanContactUs,
        InsightmanBtn,
    },
    // mounted: function () {
    //     for (var i = 0;i < object.length; i++ ){
    //         if(object[i] == '超標') this.isActive == true;
    //     }
    // },
}
</script>

<style>
@media (max-width: 899px) {
    .Report-detection {
        margin-top: 40px; 
    }
    .Report-detection h3 {
        text-align: center;
        font-size: 25px;
    }
    .Report-content {
        width: 60vw;
        height: auto;
        margin: 60px auto;
    }
    .Report-content-li {
        display: flex;
        align-items: center;
        flex-wrap: wrap;
        margin: 30px auto;
        height: 50px;
    }
    .Report-content-li h4 {
        font-size: 41px;
        color:#B3212D;
        font-weight: 400;
        float: left;
        margin: 0;
        width: 35vw;
    }
    .Report-content-li p {
        font-size: 26px;
        margin: 0;
        color: #3D953D;
    }
    
}
</style>
