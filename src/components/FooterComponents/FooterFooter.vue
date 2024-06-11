<script>
export default{
    data(){
        return {
            socialLinks: [
                {
                    id: 1,
                    title: 'Facebook',
                    image: 'footer-facebook.png',
                    url: '#'
                },
                {
                    id: 2,
                    title: 'Twitter',
                    image: 'footer-twitter.png',
                    url: '#'
                },
                {
                    id: 3,
                    title: 'Youtube',
                    image: 'footer-youtube.png',
                    url: '#'
                },
                {
                    id: 4,
                    title: 'Pinterest',
                    image: 'footer-pinterest.png',
                    url: '#'
                },
                {
                    id: 5,
                    title: 'Periscope',
                    image: 'footer-periscope.png',
                    url: '#'
                }
            ]
        }
    },
    methods: {
        getImagePath: function(img){
            return new URL(`../../assets/img/${img}`, import.meta.url).href;
        }
    },
}
</script>

<template>
    <section class="footer">
        <div class="container">
            <button>Sign-up now!</button>
            <div class="socials">
                <h2>Follow us</h2>
                <ul>
                    <li v-for="link in socialLinks" :key="link.id">
                        <a :href="link.url">
                            <img :src="getImagePath(link.image)" :alt="`${link.title} Icon`">
                        </a>
                    </li>
                </ul>
            </div>
            
        </div>
    </section>
</template>

<style lang="scss" scoped>
    @use '../../styles/partials/variables' as *;
    @use '../../styles/partials/mixins' as *;

    div.container {
        @include my-container();
        @include row-between-center();
        height: 100%;
    }
    
    section.footer {
        background-color: $bg-footer;
        padding: 2rem 0;

        button {
            text-transform: uppercase;
            background-color: transparent;
            color: white;
            padding: 1rem;
            border: 2px solid $primary-color;
            cursor: pointer;
        }

        .socials {
        @include row-center();

            h2 {
                text-transform: uppercase;
                color: $primary-color;
                margin-right: 1.5rem
            }

            ul {
                @include row-center();

                li {
                    margin: 0 .75rem;
                }
            }
        }
    }
</style>