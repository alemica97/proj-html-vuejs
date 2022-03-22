<template>
    <div id="jumbo" class="jumbotron container-fluid">
        <myHeader />
        
        <div class="container-sm px-0 px-lg-4 px-xl-5">
            <!-- la descrizione la suddivido con una row composta da 3 col, ognuna col-12  -->
            <div class="jumbo-description row text-center">
                <div class="col-12">
                    <h1 class="jumbo-title mb-4">{{ jumboTitle }}</h1>
                </div>
                <div class="col-12">
                    <p class="jumbo-paragraph mb-4">{{ jumboParagraph }}</p>
                </div>
                <div class="col-12 mt-3">
                    <button class="btn-blue">{{ jumboButton }}</button>
                </div>
            </div>
            <div class="row py-3 text-center">
                <div class="col-12">
                    <!-- tre pallini del carousel  -->
                <i class="fa-solid fa-circle mx-1"></i>
                <i class="fa-solid fa-circle mx-1"></i>
                <i class="fa-solid fa-circle active mx-1"></i>
                </div>
            </div>
        </div>
        
    </div>
</template>

<script>
import myHeader from './Header.vue'

export default {
    name: 'myJumbo',

    components: {
        myHeader,
    },

    data(){
        return{
            jumboTitle: 'Contemporary Ideas',
            jumboParagraph: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Minima similique dolorum aperiam aliquid laudantium nihil eum impedit molestias, beatae ducimus maiores quod accusamus? Voluptate nobis corrupti temporibus animi, eius ratione.',
            jumboButton: 'register now'
        }
    }
}
</script>

<style lang="scss" scoped>

    .jumbotron{
        background-image: url(../assets/icademy/icademy/img/course-9-f-img.jpg);
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;
        position: relative;
        min-height: 400px;
        z-index: 0;

        &:after {
            position: absolute;
            content: " ";
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            background-color: rgba(0, 0, 0, 0.3);
        }
        
        .jumbo-description{
            color: #ffffff;
            z-index: 999;

            .jumbo-title{
                font-size: calc(40px + 1.6vw);
                font-weight: 700;
            }
            .jumbo-paragraph{
                font-size: calc(14px + 0.3vw);
                font-weight: 400;
                color: #ffffffe0;
            }

            &.row{
                padding: 140px 15px 165px 15px;
            }
        }
    }
   
    button{  //questo è qui finché non capisco perché non funziona correttamente il file _common.scss
        font-size: calc(10px + 0.5vw);
        font-weight: 600;
    }

    .fa-solid{
        color: #ffffff4b;

        &.active{
            color: #ffffff;
        }
        &:hover{
            cursor: pointer;
        }
    }

</style>