<template>
    <div></div>
</template>

<script>
export default {
    data:()=>({
        // check_lang: ''
    }),
    mounted(){
        if(this.$i18n.locale == 'CN'){
            this.$router.push('/CN/stronghold')
        } else {
            this.$router.push('/stronghold')
        }
        // this.$router.push(this.check_lang + '/stronghold/')
    }
}
</script>

<style>

</style>