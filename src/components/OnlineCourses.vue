<template>
    <section id="online-courses" class="container-fluid">
        <div class="container-sm">
            <div class="row justify-content-center">
                <div class="col-12 col-md-10 px-3 text-center">
                    <h1 class="mb-4">{{ courseTitle }}</h1>
                    <p class="mb-5">{{ courseParagraph }}</p>
                </div>
            </div>
            <div class="card-row row gy-4 justify-content-center">
                <onlineCoursesCards 
                v-for="(card, i) in onlineCoursesCards"
                :key="i"
                :singleCard="card"/>
            </div>
            <div class="row my-4">
                <div class="carousel-index col-12 text-center">
                    <i class="fa-solid fa-circle mx-1"></i>
                    <i class="fa-solid fa-circle active mx-1"></i>
                    <i class="fa-solid fa-circle mx-1"></i>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import onlineCoursesCards from './OnlineCoursesCards.vue'

export default {
    name: 'onlineCourses',

    components:{
        onlineCoursesCards,
    },

    data(){
        return{
            courseTitle: 'Popular Online Courses',
            courseParagraph: `Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
                              sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
                              Libero volutpat sed cras ornare arcu dui vivamus arcu felis.`,

            onlineCoursesCards: [
                {
                    image: require('../assets/icademy/icademy/img/course-5-f-img.jpg'),
                    title: 'Android Developer',
                    price: 'FREE',
                    name: 'David Sanders',
                    description: `Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
                                  sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.`,
                    number: '1',
                    type: 'PROGRAMMING',
                },
                {
                    image: require('../assets/icademy/icademy/img/course-6-f-img.jpg'),
                    title: 'Web Designing',
                    price: 'FREE',
                    name: 'Jennifer Powell',
                    description: `Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
                                  sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.`,
                    number: '1',
                    type: 'PROGRAMMING',
                },
                {
                    image: require('../assets/icademy/icademy/img/course-12-f-img.jpg'),
                    title: 'Financial Modeling',
                    price: '$20',
                    name: 'Edward Bowman',
                    description: `Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
                                  sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.`,
                    number: '1',
                    type: 'BUSINESS',
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

    #online-courses{
        padding: 140px 0;
        background-image: url(../assets/icademy/icademy/img/background-pattern.jpg);
        background-position: 50% 30%;
        border-bottom: 1px solid #00000026;
    }

    .carousel-index{
        font-size: calc(10px + 0.2vw);
        color: #40C4FF4b;

        i{
            &.active{
            color: #40C4FF;
            }

            &:hover{
                cursor: pointer;
            }
        }
    }

    .card-row{
        padding: 80px 0 30px 0;
    }

    h1{
        font-size: calc(40px + 0.2vw);
        font-weight: 700;
    }

    p{
        font-size: calc(15px + 0.4vw);
        color: #595959;
    }
</style>