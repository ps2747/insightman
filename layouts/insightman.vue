<template>
  <div class="all-background">
    <insightman-header-nav></insightman-header-nav>
    <nuxt />
    <insightman-contact-us></insightman-contact-us>
  </div>
</template>

<script>
import InsightmanHeaderNav from '~/components/InsightmanHeaderNav.vue'
import InsightmanContactUs from '~/components/InsightmanContactUs.vue';
export default {
  head() {
        return  {
            // title: 'BMI計算',
            meta: [
                { charset: 'utf-8' },
                { name: 'viewport', content: 'width=device-width, initial-scale=1, maximum-scale=1.0,user-scalable=0,' },
                // { hid: 'description', name: 'description', content: '' },
                // { property : 'og:title' , content:""},
                // { property : 'og:type' , content:"education tech."},
                // { property : 'og:url' , content:"https://www.ludonow.com/mommiyoga"},
                // { property : 'og:image' , content:"https://www.ludonow.com/resume/resume-og-img.jpg"},
                // { property : 'og:description' , content:"yoga"},
                // { property : 'og:site_name' , content:"www.ludonow.com"},
            ],
            link: [
                // { rel: 'icon', type: 'image/x-icon', href: '/fc-logo.ico' }
            ],
            script: [
                // { src: 'https://player.vimeo.com/api/player.js' },
                // { id:"ze-snippet" ,src: 'https://static.zdassets.com/ekr/snippet.js?key=1254e916-e473-4d23-904e-63c6886e6497' },
            ],
        }
    },
  components: {
    InsightmanHeaderNav,
    InsightmanContactUs
  }
}
</script>


<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
@media (max-width:899px) {
  .all-background {
    background-image: url('/liner-background.jpg');
    background-repeat: no-repeat;
    background-position: center center;
    background-size: cover;
  }
}
</style>
