<script>
export default{
    data(){
        return {
            
        }
    },
    props: {
        singleCard: {
            type: Object,
            required: true
        }
    }
}
</script>

<template>
    <article>
        <div class="card-image">
            <img :src="singleCard.thumb" :alt="singleCard.series">
        </div>
        <p> {{ singleCard.series }} </p>
    </article>
</template>

<style lang="scss" scoped>
    article{
        width: calc((100% / 6) - 1rem);
        margin: 0 .5rem 3.5rem;

        .card-image{
            width: 100%;
            height: 185px;
            overflow-y: clip;
            margin-bottom: 1.2rem;

            img {
                width: 100%
            }
        }

        p{
            text-transform: uppercase;
            font-size: .8rem;
        }
    }
</style>