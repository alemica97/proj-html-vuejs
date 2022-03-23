<template>
    <section id="students-carousel" class="container-fluid">
        <div class="row container-sm mx-auto justify-content-center">
            <!-- divido la row in 4 colonne disposte una sopra l'altra, ognuna centrata orizzontalmente  -->
            <div class="col-12">
                <figure class="text-center mb-5">
                    <img :src="image" alt="">
                </figure>
            </div>

            <div class="carousel-paragraph col-12 col-md-10 text-center mb-4">
                <p>{{ carouselParagraph }}</p>
            </div>

            <div class="carousel-student col-12 text-center mb-5">
                <h4>{{ name }}</h4>
                <span class="text-uppercase">{{ category }}</span>
            </div>

            <div class="carousel-index col-12 text-center">
                <i class="fa-solid fa-circle mx-1"></i>
                <i class="fa-solid fa-circle active mx-1"></i>
                <i class="fa-solid fa-circle mx-1"></i>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'studentsCarouselSection',

    data(){
        return{
            image: require('../assets/icademy/icademy/img/testimonials-standard-2.png'),
            carouselParagraph: `Maecenas accumsan lacus vel facilisis volutpat est velit. 
                                Fringilla est ullamcorper eget nulla. Quam nulla porttitor massa 
                                id neque aliquam vestibulum morbi blandit. 
                                Tristique et egestas quis ipsum suspendisse. 
                                Aliquet porttitor lacus luctus accumsan tortor posuere ac ut consequat.`,
            name: 'Joan Collins',
            category: 'student',
       }
    }
}
</script>

<style lang="scss" scoped>
    #students-carousel{
        background-image: url(../assets/icademy/icademy/img/h5-parallax-img-1.png);
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;
        background-attachment: fixed;
        padding: 100px 0;
        color: #ffffff;
    }

    .carousel-paragraph{
        font-size: calc(14px + 0.4vw);
    }

    .carousel-student{
        h4{
            font-size: calc(20px + 0.2vw);
            font-weight: 700;
        }
        span{
            font-size: calc(13px + 0.2vw);
            font-weight: 700;
        }
    }

    .carousel-index{
        font-size: calc(10px + 0.2vw);
        color: #ffffff4b;

        i{
            &.active{
            color: #ffffff;
            }

            &:hover{
                cursor: pointer;
            }
        }
    }
</style>