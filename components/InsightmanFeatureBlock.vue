<template>
    <div class="ism-feature">
        <img :src="src" alt="">
        <h3 v-html="title">{{title}}</h3>
        <h6 v-html="content">{{content}}</h6>
    </div>
</template>

<script>
export default {
    props:{
        src: String,
        title: String,
        content: String,
    },
}
</script>

<style>
@media (max-width: 899px) {
    .ism-feature {
        width: 100vw;
        height: auto;
        text-align: center;
        margin-top: 65px;
    }
    .ism-feature img {
        display: block;
        margin: 0 auto;
    }
    .ism-feature h3 {
        font-size: 33px; 
        margin-top: 30px; 
    }
    .ism-feature h6 {
        font-size: 20px;
        font-weight: 400;
        line-height: 30px; 
    }
}
</style>
