<script>
export default {
    data(){
        return {
            message: 'Main',
        }
    }
}
</script>

<template>
    <main>
        <div class="container">
            <h1>--> Content goes here <--</h1>
        </div>
    </main>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;

    main {
        padding: 3.5rem 0;
    }

    div.container {
        @include my-container();
    }
    
</style>