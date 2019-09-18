<template>
    <div>
         <h3 class="about-company-title">{{$t('menu_about')}}</h3>
         <div style="background:#939393;padding-bottom:20px;">
            <div class="about-company-idea">
                <img src="/line-2.png" alt="">
                <h3 style="text-align:left;padding-left:30px;">{{$t('about_1_title')}}</h3>
                <p v-html="$t('about_1_text')"></p>
                <img src="/line-4.png" alt="">
            </div>
            <div class="about-company-idea" style="background:#939393;padding-top:0;">
                <h3 style="text-align:left;padding-left:30px;">{{$t('about_2_title')}}</h3>
                <p style="margin-bottom:20px;" v-html="$t('about_2_text')"></p>
            </div>
         </div>
         <img src="/line-5.png" alt="" style="width: 100vw;">
         <div>
             <h3 class="about-company-title" style="margin-top:40px;">{{$t('about_3_title')}}</h3>
             <h3 style="text-align:center;font-size:20px;margin-top:35px;">{{$t('about_3_text')}}</h3>
             <div class="about-company-team">
                 <img src="/about/about-company-team-1.png" alt="">
                 <h4 v-html="$t('about_block_1_name')"></h4>
                 <p v-html="$t('about_block_1_text')"></p>
             </div>
              <!-- <div class="about-company-team">
                 <img src="/about/about-company-team-2.png" alt="">
                 <h4>Leo Chandra<br>劉正昌</h4>
                 <p>印尼哥倫比亞集團總裁劉正昌董事長，出生於廣州梅縣。印尼“電器大王” 哥倫比亞集團是印尼最大的4c家電連鎖批發商、電器傢具摩托製造商。</p>
             </div> -->
             <div class="about-company-team">
                 <img src="/about/about-company-team-3.png" alt="">
                 <h4 v-html="$t('about_block_2_name')"></h4>
                 <p v-html="$t('about_block_2_text')"></p>
             </div>
             <!-- <div class="about-company-team">
                 <img src="/about/about-company-team-4.png" alt="">
                 <h4>資深總經理，環保理念、營養學顧問<br>郭玉麗</h4>
                 <p>負責Engine Wizard環境保護課程、養生保健講師。郭總畢生致力推動環保理念和食品養生觀念。<br>
                擁有中國國際營養師認證、台灣國立成功大學企業管理碩士學位，台灣自然醫學美容25年實務經驗、台灣分子矯正醫學23年實務經驗、台灣環保媽媽環境保護基金會台南隊長20年，現任台灣世紀美生物科技有限公司總經理。</p>
             </div> -->
             <div class="about-company-team">
                 <img style="width:123px;" src="/about/about-company-team-5.png" alt="">
                 <h4 v-html="$t('about_block_3_name')"></h4>
                 <p v-html="$t('about_block_3_text')"></p>
             </div>
             <div class="about-company-team">
                 <img src="/about/about-company-team-6.png" alt="">
                 <h4 v-html="$t('about_block_4_name')"></h4>
                 <p v-html="$t('about_block_4_text')"></p>
             </div>
             <div class="about-company-team">
                 <img src="/about/about-company-team-7.png" alt="">
                 <h4 v-html="$t('about_block_5_name')"></h4>
                 <p v-html="$t('about_block_5_text')"></p>
             </div>
         </div>
    </div>
</template>

<script>
export default {
    layout: 'insightman',
}
</script>

<style>
@media (max-width:899px) {
    .about-company-title {
        text-align: center;
        margin-top: 30px;
        font-size: 25px;
    }
    .about-company-idea {
        position: relative;
        background-color: #B3212D;
        height: auto;
        width: 100vw;
        margin-top: 50px;
        padding-top: 50px; 
    }
    .about-company-idea img:first-child {
        position: absolute;
        margin-bottom: 30px;
        top: -3px;
        width: 100vw;
    }
    .about-company-idea img:last-child {
        margin-bottom: -30px;
        width: 100vw;
    }
    .about-company-idea h3 {
        color: white;
        font-size: 22px;
        text-align: center;
    }
    .about-company-idea p {
        margin: 30px auto;
        width: 86vw;
        color: white;
        font-size: 16px;
    }
    .about-company-team {
        width: 86vw;
        margin: 50px auto 0;
    }
    .about-company-team img {
        display: block;
        margin: 0 auto 20px;
    }
    .about-company-team h4 {
        text-align: center;
        font-size: 20px;
        line-height: 30px;
    }
    .about-company-team p {
        margin-top: 30px;
        color: #707070;
    }
}
</style>
