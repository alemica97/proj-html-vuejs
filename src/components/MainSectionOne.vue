<template>
    <section class="container-fluid">
        <div class="container-xl">
            <div class="row gap-4 gap-lg-3 justify-content-center">
                <cardSectionOne 
                v-for="(element, index) in cardsElements"
                :key="index"
                :cardsEl="element"/>
            </div>
        </div>
    </section>
</template>

<script>
import cardSectionOne from './CardSectionOne.vue'

export default {
    name: 'sectionOne',

    components:{
        cardSectionOne,
    },

    data(){
        return{
            // creo un array di oggetti con gli elementi da collegare alle card 
            cardsElements: [
                {
                    image: require('../assets/icademy/icademy/img/h5-custom-icon-1.png'),
                    title: 'Languages'
                },
                {
                    image: require('../assets/icademy/icademy/img/h5-custom-icon-2.png'),
                    title: 'Software'
                },
                {
                    image: require('../assets/icademy/icademy/img/h5-custom-icon-3.png'),
                    title: 'Business'
                },
                {
                    image: require('../assets/icademy/icademy/img/h5-custom-icon-4.png'),
                    title: 'Chemistry'
                },
                {
                    image: require('../assets/icademy/icademy/img/h5-custom-icon-5.png'),
                    title: 'Science'
                },
                {
                    image: require('../assets/icademy/icademy/img/h5-custom-icon-6.png'),
                    title: 'DIY&Craft'
                }
            ],
        }
    }
}
</script>

<style lang="scss" scoped>

    .container-xl{
        padding: 30px 20px;
    }
</style>