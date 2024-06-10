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
        <section class="main-content">
            <div class="container">
                <h1>--> Content goes here <--</h1>
            </div>
        </section>
        <section class="shop-banner">
            <div class="container">
                <ul>
                    <li>
                        <img src="../assets/img/buy-comics-digital-comics.png" alt="Digital Comics">
                        <a href="#">Digital Comics</a>
                    </li>
                    <li>
                        <img src="../assets/img/buy-comics-merchandise.png" alt="Merchandise">
                        <a href="#">Merchandise</a>
                    </li>
                    <li>
                        <img src="../assets/img/buy-comics-subscriptions.png" alt="Subscription">
                        <a href="#">Subscription</a>
                    </li>
                    <li>
                        <img src="../assets/img/buy-comics-shop-locator.png" alt="Comic Shop Locator">
                        <a href="#">Comic Shop Locator</a>
                    </li>
                    <li>
                        <img src="../assets/img/buy-dc-power-visa.svg" alt="DC Power Visa">
                        <a href="#">DC Power Visa</a>
                    </li>
                </ul>
            </div>
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

        ul {
            @include row-between-center();
            padding: 3rem;

            li {
                @include row-center();
                width: calc(100% / 6);
            }

            img {
                margin-right: 1rem;
                width: 50px;
                height: 55px;
            }

            a {
                text-transform: uppercase;
                color: white;
                font-size: .8rem;
            }

            a:hover{
                text-decoration: underline;
            }
        }
    }
    
</style>