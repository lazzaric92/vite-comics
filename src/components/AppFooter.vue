<script>
export default {
    data(){
        return {
            message: 'Footer',
        }
    }
}
</script>

<template>
    <footer>
        <section class="footer-nav">
            <div class="container">
                <div class="nav-wrapper">
                    <nav>
                        <h2>DC Comics</h2>
                        <ul>
                            <li>
                                <a href="#">link</a>
                            </li>
                            <li>
                                <a href="#">link</a>
                            </li>
                            <li>
                                <a href="#">link</a>
                            </li>
                            <li>
                                <a href="#">link</a>
                            </li>
                            <li>
                                <a href="#">link</a>
                            </li>
                        </ul>
                    </nav>
                    <nav>
                        <h2>DC Comics</h2>
                        <ul>
                            <li>
                                <a href="#">link</a>
                            </li>
                            <li>
                                <a href="#">link</a>
                            </li>
                        </ul>
                    </nav>
                    <nav>
                        <h2>DC Comics</h2>
                        <ul>
                            <li>
                                <a href="#">link</a>
                            </li>
                            <li>
                                <a href="#">link</a>
                            </li>
                            <li>
                                <a href="#">link</a>
                            </li>
                            <li>
                                <a href="#">link</a>
                            </li>
                            <li>
                                <a href="#">link</a>
                            </li>
                            <li>
                                <a href="#">link</a>
                            </li>
                            <li>
                                <a href="#">link</a>
                            </li>
                        </ul>
                    </nav>
                    <nav>
                        <h2>DC Comics</h2>
                        <ul>
                            <li>
                                <a href="#">link</a>
                            </li>
                            <li>
                                <a href="#">link</a>
                            </li>
                            <li>
                                <a href="#">link</a>
                            </li>
                            <li>
                                <a href="#">link</a>
                            </li>
                            <li>
                                <a href="#">link</a>
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
                        <li>
                            <a href="#">
                                <img src="../assets/img/footer-facebook.png" alt="Facebook Icon">
                            </a>
                        </li>
                        <li>
                            <img src="../assets/img/footer-twitter.png" alt="Twitter Icon">
                        </li>
                        <li>
                            <img src="../assets/img/footer-youtube.png" alt="Youtube Icon">
                        </li>
                        <li>
                            <img src="../assets/img/footer-pinterest.png" alt="Pinterest Icon">
                        </li>
                        <li>
                            <img src="../assets/img/footer-periscope.png" alt="Periscope Icon">
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
                margin-right: 3rem;
                margin-bottom: .75rem;

                h2 {
                    margin-bottom: 1rem;
                }

                li {
                    margin-bottom: .3rem;
                }
            }
        }

        a {
            color: $font-grey;
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