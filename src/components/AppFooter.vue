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

            </div>
        </section>
        <section class="footer">
            <div class="container">
                <button>Sign-up now!</button>
                <div class="socials">
                    <h2>Follow us</h2>
                    <ul>
                        <li>
                            <img src="../assets/img/footer-facebook.png" alt="Facebook Icon">
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
    }

    footer {
        background-image: url(../assets/img/footer-bg.jpg)
    }

    section.footer {
        background-color: $bg-footer;
        padding: 2rem 0;

        div.container {
            @include row-between-center;

            button {
                text-transform: uppercase;
                background-color: transparent;
                color: white;
                padding: 1rem;
                border: 2px solid $primary-color;
            }
        }
    }

    .socials {
        @include row-center;

        h2 {
            text-transform: uppercase;
            color: $primary-color;
            margin-right: 1.5rem
        }

        ul {
            @include row-center;

            li {
                margin: 0 .75rem;
            }
        }
    }

</style>