<script>
import ShopBanner from './MainComponents/ShopBanner.vue';
import MainJumbotron from './MainComponents/MainJumbotron.vue';
import MainContent from './MainComponents/MainContent.vue';


export default {
    data(){
        return {
            
        }
    },
    components: {
        ShopBanner,
        MainJumbotron,
        MainContent,
    }
}
</script>

<template>
    <main>
        <MainJumbotron />
        <MainContent />
        <ShopBanner />
    </main>
</template>

<style lang="scss" scoped>
    
</style>