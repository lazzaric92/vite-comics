<script>
export default {
    data(){
        return {
            shopLinks: [
                {
                    id: 1,
                    title: 'Digital Comics',
                    image: './src/assets/img/buy-comics-digital-comics.png',
                    url: '#'
                },
                {
                    id: 2,
                    title: 'Merchandise',
                    image: './src/assets/img/buy-comics-merchandise.png',
                    url: '#'
                },
                {
                    id: 3,
                    title: 'Subscription',
                    image: './src/assets/img/buy-comics-subscriptions.png',
                    url: '#'
                },
                {
                    id: 4,
                    title: 'Comic Shop Locator',
                    image: './src/assets/img/buy-comics-shop-locator.png',
                    url: '#'
                },
                {
                    id: 5,
                    title: 'DC Power Visa',
                    image: './src/assets/img/buy-dc-power-visa.svg',
                    url: '#'
                }
            ]
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
                    <li v-for="link in shopLinks" :key="link.id">
                        <img :src="link.image" :alt="link.title">
                        <a :href="link.url"> {{ link.title }} </a>
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
                font-size: .85rem;
            }

            a:hover{
                text-decoration: underline;
            }
        }
    }
    
</style>