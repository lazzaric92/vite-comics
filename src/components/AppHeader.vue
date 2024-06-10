<script>
export default{
data(){
    return {
        headerLinks: [
            {
                id: 1,
                title: 'characters',
                active: false,
                url: '#'
            },
            {
                id: 2,
                title: 'comics',
                active: true,
                url: '#'
            },
            {
                id: 3,
                title: 'movies',
                active: false,
                url: '#'
            },
            {
                id: 4,
                title: 'tv',
                active: false,
                url: '#'
            },
            {
                id: 5,
                title: 'games',
                active: false,
                url: '#'
            },
            {
                id: 6,
                title: 'collectibles',
                active: false,
                url: '#'
            },
            {
                id: 7,
                title: 'videos',
                active: false,
                url: '#'
            },
            {
                id: 8,
                title: 'fans',
                active: false,
                url: '#'
            },
            {
                id: 9,
                title: 'news',
                active: false,
                url: '#'
            },
            {
                id: 10,
                title: 'shop',
                active: false,
                url: '#'
            }
        ]
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
                    <li v-for="link in headerLinks" :key="link.id" :class="(link.active) ? 'active' : ''">
                        <a href="#"> {{ link.title }} </a>
                    </li>
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
            margin: 0 .75rem;
            padding: 3rem 0;
            border-bottom: 5px solid transparent;
            font-size: .85rem;
            font-weight: bold;

            &.active {
                border-bottom-color: $primary-color;
            }

            a {
                color: $bg-footer;
            }
        }
    }
</style>