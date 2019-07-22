<template>
    <div>
        <h3 class="findhold-title">搜尋結果</h3>
        <insightman-stronghold-block title="insightman汽車保養廠"
        map="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3672.969634200187!2d120.19741041580764!3d22.98814408497053!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x346e767c79ddd19f%3A0x7de2ed500e982b83!2zNzAw5Y-w5Y2X5biC5Lit6KW_5Y2A5rC456aP6Lev5LiA5q61MTg56Jmf!5e0!3m2!1szh-TW!2stw!4v1563769977725!5m2!1szh-TW!2stw"
        adress="70051 台南市中西區永福路一段189號7樓B2" phone="0800-251-490"
        style="margin:20px auto;"></insightman-stronghold-block>
        <insightman-btn title="預約體驗" bgColor="#FBEF41" bdColor="black"></insightman-btn>
    </div>
</template>

<script>
import InsightmanStrongholdBlock from '~/components/InsightmanStrongholdBlock.vue'
import InsightmanBtn from '~/components/InsightmanBtn.vue'
export default {
    layout: 'insightman',
    components:{
        InsightmanStrongholdBlock,
        InsightmanBtn,
    }
}
</script>

<style>
@media (max-width: 899px) {
    .findhold-title {
        text-align: center;
        margin-top: 30px;
        font-size: 25px;
    }
}
</style>
