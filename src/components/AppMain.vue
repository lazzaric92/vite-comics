<script>
import ShopBanner from './ShopBanner.vue'
export default {
    data(){
        return {
            
        }
    },
    components: {
        ShopBanner,
    }
}
</script>

<template>
    <main>
        <section class="main-content">
            <div class="container">
                <h1>--> Content goes here <--</h1>
            </div>
        </section>
        <section class="shop-banner">
            <ShopBanner />
        </section>
    </main>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;


    div.container {
        @include my-container();
    }

    .main-content {
        padding: 3.5rem 0;
    }

    .shop-banner {
        background-color: $primary-color;
    }
    
</style>