<script>
import SingleCard from './SingleCard.vue';

export default{
    data(){
        return {
        
        }
    },
    components: {
        SingleCard
    }
}
</script>

<template>
    <section class="main-content">
        <div class="container">
            <h1>--> Content goes here <--</h1>
            <SingleCard />
        </div>
    </section>
</template>

<style lang="scss" scoped>
    @use '../../styles/partials/variables' as *;
    @use '../../styles/partials/mixins' as *;


    div.container {
        @include my-container();
    }

    .main-content {
        padding: 3.5rem 0;
    }
</style>