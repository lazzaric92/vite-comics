<script>
export default{
data(){
    return {
        message: 'Header',
    }
}
}
</script>

<template>
    <header>
        <div class="container">
            <img src="../assets/img/dc-logo.png" alt="DC Comics Logo">
            <nav>
                <ul>
                    <li>
                        <a href="#">link</a>
                    </li>
                    <li class="active"><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;

    header {
        background-color: white;
    }

    div.container {
        @include my-container();
        @include row-between-center();
        }

    img {
        width: 85px
    }

    nav ul {
        @include row-center();

        li {
            text-transform: uppercase;
            margin: 0 1rem;
            padding: 3rem 0;
            border-bottom: 5px solid transparent;

            &.active {
                border-bottom-color: $primary-color;
            }
        }
    }
</style>