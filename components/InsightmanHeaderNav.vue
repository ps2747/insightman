<template>
    <div class="ism-header">
        <div class="ism-header-hamburger">
            <img src="/header-hamburger.png" alt="">
        </div>
        <div class="ism-header-logo">
            <img src="/header-logo.png" alt="">
        </div>
        <div class="ism-header-hamburger">
            <img src="/header-earth.png" alt="">
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>
@media (max-width: 899px) {
    .ism-header {
        width: 100vw;
        height: 70px;
        /* background: red;  */
        display: inline-flex;
        justify-content: space-around;
        align-items: center;
    }
    .ism-header-logo img {
        height: 40px;
    }
}
</style>
