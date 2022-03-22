<template>
    <section id="courser" class="container-fluid">
        <div class="top">
            <a href="#jumbo">
                <i class="fa-solid fa-chevron-up"></i>
                <span>TOP</span>
            </a>
        </div>
        <div class="container-xl  py-5 px-0 px-lg-4">
            <div class="row gap-4 gap-lg-3 justify-content-center">
                <!-- faccio un v-for sul componente figlio cardSectionOne per stamparmi dinamicamente tutte le card  -->
                <coursesCard 
                v-for="(element, index) in cardsElements"
                :key="index"
                :cardsEl="element"/>
            </div>
            <div class="row tutoring px-4 px-md-5 px-lg-0">
                <div class="col-12 col-md-8 col-lg-6">
                    <h1 class="mb-4">{{ courseSectionTitle }}</h1>
                </div>
                <div class="col-12">
                    <p>{{ courseSectionParagraph }}</p>
                </div>
                <div class="col-12 mt-3">
                    <button class="btn-transparent">{{ courseButton }}</button>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import coursesCard from './CoursesCard.vue'

export default {
    name: 'coursesSection',

    components:{
        coursesCard ,
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

            courseSectionTitle: 'The Trusted Name for In-Home Tutoring.',
            courseSectionParagraph: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Minima similique dolorum aperiam aliquid laudantium nihil eum impedit molestias, beatae ducimus maiores quod accusamus? Voluptate nobis corrupti temporibus animi, eius ratione.',
            courseButton: 'learn more',
        }
    }
}
</script>

<style lang="scss" scoped>

    #courser{
        position: relative;

        .top{
            width: 70px;
            height: 70px;
            background-color: #40C4FF;
            position: absolute;
            right: 0;
            bottom: 20%;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;

            & span{
                display: block;
            }

            & a{
                text-decoration: none;
                text-align: center;
                color: #ffffff;
                font-size: 17px;
                font-weight: 700;
            }

        }
    }
    .container-xl{
        min-height: 1500px;
        background-image: url(../assets/icademy/icademy/img/h5-img-1.jpg);
        background-repeat: no-repeat;
        background-size: contain;
        background-position: 50% 100%;
    }

    .tutoring{
        padding: 90px 0 0 0;
        // min-height: 800px;

        h1{
            font-size: calc(38px + 1vw);
            font-weight: 600;
        }
         p{
             font-size: calc(14px + 0.4vw);
             color: #3E3E3E;
         }
    }

    button{
        text-transform: uppercase;
        font-weight: 600;
        padding: 0;
    }
</style>