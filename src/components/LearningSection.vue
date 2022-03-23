<template>
    <section id="learning" class="container-fluid">
        <div class="container-sm">
            <div class="row align-items-center">
                <div class="col-12 col-md-3 mb-4 mb-md-0">
                    <div class="row p-2 p-md-0">
                        <div class="possibilities-title col-4 col-md-12"
                        v-for="(element, i) in possibilitiesTitle"
                        :key="i" @click="activeIndex = i"
                        :class="activeIndex == i ? 'active' : ''">
                            <span>{{ element }}</span>
                        </div>
                    </div>
                </div>
                <div class="possibilities-info col-12 col-md-9 p-4 p-md-5">
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

    #learning{
        border-bottom: 1px solid #00000026;
    }

    .container-sm{
        padding: 140px 0;
    }

    .possibilities-info{
        p{
            font-size: calc(15px + 0.4vw);
        }

        h1{
            font-size: calc(40px + 0.2vw);
            font-weight: 700;
        }
    }

    .possibilities{

        i{
            color: #40C4FF;
        }
    }

    .possibilities-title{
        border-top: 1px solid #E6E6E6;//provare outline
        border-right: 1px solid #E6E6E6;
        border-left: 1px solid #E6E6E6;
        display: flex;
        justify-content: flex-start;
        align-items: center;
        font-size: calc(14px + 0.5vw);
        font-weight: 700;
        padding-left: 30px;
        &:last-child{
            border-bottom: 1px solid #E6E6E6;
        }

        &:hover{
            cursor: pointer;
        }

        &.active{
            background-color: #FCFCFC;
            color: #40C4FF;
            border-left: 8px solid #40C4FF;
            & span{
                transform: translateX(-8px);
            }
        }
    }

    @media screen and (max-width: 768px){       
        [class*='col-4']{
            height: 85px;
        }
        .possibilities-title{
            padding-left: 0px;
            justify-content: center;
            border-top: 1px solid #E6E6E6;
            border-right: 1px solid #E6E6E6;
            border-left: 1px solid #E6E6E6;
            border-bottom: 1px solid #E6E6E6;

            & span{
                    padding-left: 5px;
                }
            &.active{
                border-left: 0px;
                border-top: 8px solid #40C4FF;
                border-left: 1px solid #E6E6E6;
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