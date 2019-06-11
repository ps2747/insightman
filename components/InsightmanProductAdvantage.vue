<template>
    <div class="ism-product-advantage">
        <img src="/aboutProduct/background-line-1.png" alt="">
        <div class="product-advantage-content">
            <h4>地球上稀有離子元素！<br>非石化性質成份！</h4>
            <p>不含毒素、重金屬和強化物，不含有任何金屬分子、固體成份及化學成份的液態元素。<br><br>可與任何油(脂)、液壓油、切削油、合成油等混合，作用週期持久且沒有副作用。<br><br>引擎在內熱和壓力的作用下(引擎開始損耗、減分中)，獨特的『運行中保養』功能就會被啟動。</p>
            <h4>油泥的剋星</h4>
            <p>離子能滲入金屬表面細孔，有效填平金屬表面微孔，改變金屬表面的分子結構，消除積碳、油泥...等，在磨損表面進行優質化，減少解體維修、塘缸大修的效果。</p>
            <h4>舊車的福星</h4>
            <p>5年10萬公里以上老舊車輛，如沉積嚴重之引擎，每次更換機油後，再添加一瓶 30 公克引擎精靈，引擎將會超安靜、潤滑，有如新車一樣好開。</p>
        </div>
        <img src="/aboutProduct/background-line-2.png" alt="">
    </div>
</template>

<script>
export default {

}
</script>

<style>
@media (max-width: 899px) {
    .ism-product-advantage {
        position: relative;
        background: #FBEF41;
        height: auto;
        margin-top: 70px; 
        padding-top:10px; 
        padding-bottom: 20px;
    }
    .ism-product-advantage img:first-child {
        position: absolute;
        width: 100vw;
        top: -40px;
    }
    .product-advantage-content {
        /* background: red; */
        width: 86vw;
        height: auto;
        margin: 30px auto;
    }
    .product-advantage-content h4 {
        font-size: 29px;
        line-height: 40px;
        margin-top: 30px;
    }
    .product-advantage-content p {
        margin-top:30px;
        font-size: 20px;
    } 
    .ism-product-advantage img:last-child {
        position: absolute;
        width: 100vw;
        bottom: -30px;
    }
}
</style>
