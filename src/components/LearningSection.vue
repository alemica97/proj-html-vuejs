<template>
    <section id="learning" class="container-fluid">
        <div class="container-sm px-0 px-md-2 px-lg-4">
            <div class="row align-items-center">
                <div class="col-12 col-md-3 mb-5 mb-md-0">
                    <div class="row p-2 p-md-0">
                        <div class="possibilities-title col-4 col-md-12"
                        v-for="(element, i) in possibilitiesTitle"
                        :key="i" @click="activeIndex = i"
                        :class="activeIndex == i ? 'active' : ''">
                            <span>{{ element }}</span>
                        </div>
                    </div>
                </div>
                <div class="possibilities-info col-12 col-md-9">
                    <h1 class="mb-4">{{ infoTitle }}</h1>
                    <p class="mb-5">{{ infoParagraph }}</p>
                    <p class="possibilities" 
                    v-for="(element, i) in possibilitiesDescription"
                    :key="i">
                        <i class="fa-solid fa-check"></i>
                        {{ element }}
                    </p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'learningSection',    

    data(){
        return{
            possibilitiesDescription: [
                'We enrich lives through learning.',
                'Maximizing potential through individual attention.',
                'The trusted name for specialized training.',
                'People teach. People learn. This is where they connect.'
            ],

            possibilitiesTitle: [
                'What We Do',
                'Degree Programme',
                'Career Achievements',
                'Personal Managment',
                'Steps To Success',
                'Knowledge Transfer'
            ],

            activeIndex: 0,

            infoTitle: 'Learning Possibilities',
            infoParagraph: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. 
                            Saepe quia sapiente a nihil id eos at nemo ipsum voluptatem 
                            vero repellendus assumenda modi temporibus accusantium aliquam cum, 
                            quidem rerum perferendis.`,
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/variables.scss';

    #learning{
        border-bottom: 1px solid $section-border;
    }

    .container-sm{
        padding: 140px 0;
        background-image: url(../assets/icademy/icademy/img/h12-tabs-icon-1.png);
        background-repeat: no-repeat;
        background-position: 92% 80%;
        background-size: calc(120px + 1vw);
        color: #847B7B;
    }

    .possibilities-info{
        p{
            font-size: $main-par;
        }

        h1{
            font-size: $main-title;
            font-weight: 700;
            color: $title-dark;
        }
    }

    .possibilities{

        i{
            color: $colore-principale;
            margin-right: 8px;
        }
    }

    .possibilities-title{
        border-top: 1px solid $column-border;//provare outline
        border-right: 1px solid $column-border;
        border-left: 1px solid $column-border;
        background-color: white;
        display: flex;
        justify-content: flex-start;
        align-items: center;
        font-size: calc(14px + 0.5vw);
        font-weight: 700;
        padding-left: 30px;
        &:last-child{
            border-bottom: 1px solid $column-border;
        }

        &:hover{
            cursor: pointer;
        }

        &.active{
            background-color: $column-bkc;
            color: $colore-principale;
            border-left: 8px solid $colore-principale;
            & span{
                transform: translateX(-8px);
            }
        }

        &:hover span{
            transform: scale(1.03, 1.03);
            transition: all 500ms;
        }
    }

    @media screen and (max-width: 768px){       
        [class*='col-4']{
            height: 85px;
        }
        .possibilities-title{
            padding-left: 0px;
            justify-content: center;
            border-top: 1px solid $column-border;
            border-right: 1px solid $column-border;
            border-left: 1px solid $column-border;
            border-bottom: 1px solid $column-border;

            & span{
                    padding-left: 5px;
                }
            &.active{
                border-left: 0px;
                border-top: 8px solid $colore-principale;
                border-left: 1px solid $column-border;
                & span{
                    transform: translateX(0);
                }
            }
        }
    }

    @media screen and (min-width: 769px){       
        [class*='col-md-12']{
            height: 85px;
        }
    }
</style>