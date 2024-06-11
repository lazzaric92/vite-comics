<script>
export default {
    data(){
        return {
            navs: [
                {
                    title : 'DC Comics', 
                    links : [
                        {
                            id: 1,
                            title: 'Characters',
                            url: '#'
                        },
                        {
                            id: 2,
                            title: 'Comics',
                            url: '#'
                        },
                        {
                            id: 3,
                            title: 'Movies',
                            url: '#'
                        },
                        {
                            id: 4,
                            title: 'Tv',
                            url: '#'
                        },
                        {
                            id: 5,
                            title: 'Games',
                            url: '#'
                        },
                        {
                            id: 6,
                            title: 'Videos',
                            url: '#'
                        },
                        {
                            id: 7,
                            title: 'News',
                            url: '#'
                        }
                    ],
                },
                {
                    title: 'Shop',
                    links: [
                        {
                            id: 1,
                            title: 'Shop DC',
                            url: '#'
                        },
                        {
                            id: 2,
                            title: 'Shop DC Collectibles',
                            url: '#'
                        }
                    ],
                },
                {
                    title:'DC',
                    links: [
                        {
                            id: 1,
                            title: 'Terms Of Use',
                            url: '#'
                        },
                        {
                            id: 2,
                            title: 'Privacy policy (New)',
                            url: '#'
                        },
                        {
                            id: 3,
                            title: 'Ad Choices',
                            url: '#'
                        },
                        {
                            id: 4,
                            title: 'Advertising',
                            url: '#'
                        },
                        {
                            id: 5,
                            title: 'Jobs',
                            url: '#'
                        },
                        {
                            id: 6,
                            title: 'Subscriptions',
                            url: '#'
                        },
                        {
                            id: 7,
                            title: 'Talent Workshops',
                            url: '#'
                        },
                        {
                            id: 8,
                            title: 'CPSC Certificates',
                            url: '#'
                        },
                        {
                            id: 9,
                            title: 'Ratings',
                            url: '#'
                        },
                        {
                            id: 10,
                            title: 'Shop Help',
                            url: '#'
                        },
                        {
                            id: 11,
                            title: 'Contact Us',
                            url: '#'
                        }
                    ],
                },
                {
                    title:'Sites',
                    links: [
                    {
                            id: 1,
                            title: 'DC',
                            url: '#'
                        },
                        {
                            id: 2,
                            title: 'MAD Magazine',
                            url: '#'
                        },
                        {
                            id: 3,
                            title: 'DC Kids',
                            url: '#'
                        },
                        {
                            id: 4,
                            title: 'DC Universe',
                            url: '#'
                        },
                        {
                            id: 5,
                            title: 'DC Power Visa',
                            url: '#'
                        }
                    ],
                }
            ],
            socialLinks: [
                {
                    id: 1,
                    title: 'Facebook',
                    image: './src/assets/img/footer-facebook.png',
                    url: '#'
                },
                {
                    id: 2,
                    title: 'Twitter',
                    image: './src/assets/img/footer-twitter.png',
                    url: '#'
                },
                {
                    id: 3,
                    title: 'Youtube',
                    image: './src/assets/img/footer-youtube.png',
                    url: '#'
                },
                {
                    id: 4,
                    title: 'Pinterest',
                    image: './src/assets/img/footer-pinterest.png',
                    url: '#'
                },
                {
                    id: 5,
                    title: 'Periscope',
                    image: './src/assets/img/footer-periscope.png',
                    url: '#'
                }
            ]
        }
    }
}
</script>

<template>
    <footer>
        <section class="footer-nav">
            <div class="container">
                <div class="nav-wrapper">
                    <nav v-for="(nav, index) in navs" :key="nav.index">
                        <h2> {{ nav.title }} </h2>
                        <ul>
                            <li v-for="link in nav.links" :key="link.id">
                                <a :href="link.url">
                                    {{ link.title }}
                                </a>
                            </li>
                        </ul>
                    </nav>
                </div>
                <img src="../assets/img/dc-logo-bg.png" alt="DC Comics Logo">
            </div>
        </section>
        <section class="footer">
            <div class="container">
                <button>Sign-up now!</button>
                <div class="socials">
                    <h2>Follow us</h2>
                    <ul>
                        <li v-for="link in socialLinks" :key="link.id">
                            <a :href="link.url">
                                <img :src="link.image" :alt="`${link.title} Icon`">
                            </a>
                        </li>
                    </ul>
                </div>
                
            </div>
        </section>
    </footer>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;

    div.container {
        @include my-container();
        @include row-between-center();
        height: 100%;

    }

    section.footer-nav{
        background-image: url(/src/assets/img/footer-bg.jpg);
        background-size: cover;
        height: 375px;
        overflow-y: clip;

        .nav-wrapper {
            display: flex;
            flex-flow: column wrap;
            height: 100%;
            padding: 3rem 0;

            nav {
                margin-right: 2rem;
                margin-bottom: .5rem;

                h2 {
                    margin-bottom: .8rem;
                    text-transform: uppercase;
                    font-size: 1.2rem;
                }

                li {
                    margin-bottom: .3rem;
                    font-size: .8rem;
                }
            }
        }

        a {
            color: $font-grey;
        }

        a:hover{
            text-decoration: underline;
            color: white;
        }
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