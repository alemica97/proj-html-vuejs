<template>
    <div class="card col-5 col-sm-3 col-lg-1 
    align-items-center justify-content-center
    gap-4">
        <figure>
            <img :src="cardsEl.image" alt="">
        </figure>
        <h3>{{ cardsEl.title }}</h3>
    </div>
</template>

<script>
export default {
    name: 'coursesCard',

    props:{
        cardsEl:{
            type: Object,
        }
    },

}
</script>

<style lang="scss" scoped>
@import '../assets/scss/variables.scss';

    figure{
        max-width: 80px;
        aspect-ratio: 1/1;
    }

    .card{
        border: 1px solid $cards-border;
        border-radius: 0;
        aspect-ratio: 4/5;
        background-color: $cards-bkc;
        padding: 20px;

        h3{
            font-size: calc(14px + 0.4vw);
            font-weight: 700;
        }
    }

    @media screen and (min-width: 992px){
        .col-lg-1 {
            flex: 0 0 auto;
            width: calc((100% / 6) - 1rem);
        }
    }

</style>