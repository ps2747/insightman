<template>
    <div class="insightman-member-page">
        <insightman-header-nav></insightman-header-nav>
        <div class="insightman-member-use">
            <h4>會員中心</h4>
            <div class="insightman-member-use-select">
                <div class="insightman-member-use-icon">
                    <div>
                        <img src="/member/member-icon-1.svg" alt="">
                    </div>
                    <p>訂單管理</p>
                </div>
                <div class="insightman-member-use-icon">
                    <div>
                        <img src="/member/member-icon-2.svg" alt="">
                    </div>
                    <p>檢測紀錄</p>
                </div>
                <div class="insightman-member-use-icon">
                    <div>
                        <img src="/member/member-icon-3.svg" alt="">
                    </div>
                    <p>購物車</p>
                </div>

                <div class="insightman-member-use-icon">
                    <div>
                        <img src="/member/member-icon-4.svg" alt="">
                    </div>
                    <p>通知中心</p>
                </div>
                <div class="insightman-member-use-icon">
                    <div>
                        <img src="/member/member-icon-5.svg" alt="">
                    </div>
                    <p>常用地址</p>
                </div>
                <div class="insightman-member-use-icon">
                    <div>
                        <img src="/member/member-icon-6.svg" alt="">
                    </div>
                    <p>預約管理</p>
                </div>

                <div class="insightman-member-use-icon">
                    <div>
                        <img src="/member/member-icon-7.svg" alt="" style="width:70%">
                    </div>
                    <p>付款設定</p>
                </div>
                <div class="insightman-member-use-icon">
                    <div>
                        <img src="/member/member-icon-8.svg" alt="" >
                    </div>
                    <p>基本設定</p>
                </div>
                <div class="insightman-member-use-icon">
                    <div>
                        <img src="/member/member-icon-9.svg" alt="" style="height:75%">
                    </div>
                    <p>登出</p>
                </div>
            </div>
        </div>
        <router-link to="/detection" style="text-decoration: none;">
            <insightman-btn title="開始檢測" bgColor="#FBEF41" bdColor="black"></insightman-btn>
        </router-link>
        <insightman-only-footer></insightman-only-footer>
    </div>
</template>

<script>
import InsightmanHeaderNav from '~/components/InsightmanHeaderNav.vue';
import InsightmanOnlyFooter from '~/components/InsightmanOnlyFooter.vue';
import InsightmanBtn from '~/components/InsightmanBtn.vue';
export default {
    components: {
        InsightmanHeaderNav,
        InsightmanOnlyFooter,
        InsightmanBtn,
    },
}
</script>

<style>
@media (max-width:899px) {
    .insightman-member-page {
        position: relative;
        width: 100vw;
        height: 100vh;
        overflow: hidden;
    }
    .insightman-member-use {
        width: 85vw;
        height: 60vh;
        /* background: red; */
        margin: 2vh auto 3vh;
    }
    .insightman-member-use h4 {
        font-size: 23px;
        font-weight: 500;
        text-align: center;
    }
    .insightman-member-use-select {
        width: 85vw;
        height: 50vh;
        /* background: green; */
        display: flex;
        flex-wrap: wrap;
        justify-content: space-evenly;
        align-items: center;
        margin-top: 2vh;
    }
    .insightman-member-use-icon {
        /* background: yellow; */
        width: 27vw;
        height: 12vh;
        display: flex;
        flex-wrap: wrap;
        align-items: initial;
        justify-content: center;
        /* padding-top: 2vh; */
        
    }
    .insightman-member-use-icon div {
        height: 7vh;
        width: 60%;
        /* background: white; */
        margin-bottom: 5px;
    }
    .insightman-member-use-icon img {
        width: 90%;
        height: 85%;
        margin: 0 auto;
        display: block;
    }
    .insightman-member-use-icon p {
        width: 100%;
        text-align: center;
        font-size: 14px; 
    }
}
</style>
