<template>
    <div class="ism-contact-page">
        <insightman-header-nav></insightman-header-nav>
        <h3 class="about-company-title">{{$t('menu_contact')}}</h3>
        <insightman-contact-us class="contact-bottom-block"></insightman-contact-us>
    </div>
</template>

<script>
import InsightmanHeaderNav from '~/components/InsightmanHeaderNav.vue'
import InsightmanContactUs from '~/components/InsightmanContactUs.vue';
export default {
    components: {
        InsightmanHeaderNav,
        InsightmanContactUs,
    }  
} 
</script>

<style>
@media (max-width: 899px) {
    .ism-contact-page {
        background-image: url('/liner-background.jpg');
        background-repeat: no-repeat;
        background-position: center center;
        background-size: cover;
    }
    .contact-bottom-block.ism-contactus h3 {
        display: none;
    }
    .about-company-title {
        text-align: center;
        margin-top: 30px;
        font-size: 25px;
    }
}
</style>