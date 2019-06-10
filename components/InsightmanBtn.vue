<template>
    <div class="ism-button-box">
        <button v-html="title" :style="{backgroundColor:bgColor,borderColor:bdColor}" class="ism-button">{{title}}</button>
    </div>
</template>

<script>
export default {
    props:{
        title: String,
        bgColor: String,
        bdColor: String,
    }
}
</script>

<style>
@media (max-width:899px) {
    .ism-button {
        width: 150px;
        height: 50px;
        border: solid;
        border-radius: 25px;
        display: block;
        margin: auto;
        font-size: 21px;
        font-weight: bold;
    }
}
</style>
