<script>
export default{
    data(){
        return {
            shopLinks: [
                {
                    id: 1,
                    title: 'Digital Comics',
                    image: 'buy-comics-digital-comics.png',
                    url: '#'
                },
                {
                    id: 2,
                    title: 'Merchandise',
                    image: 'buy-comics-merchandise.png',
                    url: '#'
                },
                {
                    id: 3,
                    title: 'Subscription',
                    image: 'buy-comics-subscriptions.png',
                    url: '#'
                },
                {
                    id: 4,
                    title: 'Comic Shop Locator',
                    image: 'buy-comics-shop-locator.png',
                    url: '#'
                },
                {
                    id: 5,
                    title: 'DC Power Visa',
                    image: 'buy-dc-power-visa.svg',
                    url: '#'
                }
            ]
        }
    },
    methods: {
        getImagePath: function(img){
            return new URL(`../../assets/img/${img}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <section class="shop-banner">
        <div class="container">
            <ul>
                <li v-for="link in shopLinks" :key="link.id">
                    <img :src="getImagePath(link.image)" :alt="link.title">
                    <a :href="link.url"> {{ link.title }} </a>
                </li>
            </ul>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    @use '../../styles/partials/variables' as *;
    @use '../../styles/partials/mixins' as *;

    .shop-banner {
        background-color: $primary-color;
    }

    div.container {
        @include my-container();
    }

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
</style>