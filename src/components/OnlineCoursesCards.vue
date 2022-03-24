<template>
    <div class="col-9 col-md-4">
        <div class="card-wrapper"
        :class="isFree() ? '' : 'not-free'">
            <figure>
            <img :src="singleCard.image" alt="">
            </figure>
            <div class="card-info">
                <div class="teacher">
                    <span>{{singleCard.title}}</span>
                    <span>{{singleCard.name}}</span>
                </div>
                <div class="card-price">
                    <span>{{singleCard.price}}</span>
                </div>
            </div>
            <div class="card-paragraph">
                <p>{{singleCard.description}}</p>
            </div>
            <div class="card-type">
                <span><i class="fa-solid fa-user"></i>{{singleCard.number}}</span>
                <span><i class="fa-solid fa-tag"></i>{{singleCard.type}}</span>
            </div>
            </div>
    </div>
</template>

<script>
export default {
    name: 'onlineCoursesCards',

    props:{
        singleCard: Object,
    },

    methods:{
        // controllo che la stringa sia FREE, se non lo è aggiungo la classe not-free per cambiare bkc 
        isFree: function(){
            if(this.singleCard.price == 'FREE'){
                return true;
            }else{
                return false;
            }
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/variables.scss';

    .card-info{
        display: flex;
        justify-content: space-between;
        align-items: baseline;
        padding: 28px 12px;

        .teacher{
            display: flex;
            flex-direction: column;
            flex-grow: 1;

            & span:first-child{
                font-size: calc(15px + 0.4vw);
                font-weight: 700;
                color: $par-dark;
            }

            & span:last-child{
                color: #BEBEBE;
                font-weight: 700;
            }
        }

        .card-price{
            width: 55px;
            height: 24px;
            text-align: center;
            line-height: 26px;
            font-size: 14px;
            color: white;
            background-color: #FFD740;
            font-weight: 700;
            border-radius: 20px;
        }
    }

    .not-free .card-price{
        background-color: $colore-principale;
    }
    .card-paragraph{
        padding: 0 12px 28px 12px;
    }

    .card-type{
        white-space: nowrap;
        padding: 0 12px;
        margin-bottom: 35px;
        font-size: 14px;
        font-weight: 700;
        color: #B9B9B9;
        span{
            margin-right: 20px;
        }
        i{
            margin-right: 8px;
        }
    }

    

    .card-wrapper{
        color: #847B7B;
        border: 1px solid $cards-border;
        background-color: white;
        overflow: hidden;

        &:hover{
            cursor: pointer;
            figure{
                transform: scale(1.1, 1.1);
                transition: all 800ms;
            }
        }

        figure{
            position: relative;
        }

        figure::after{
            content: '';
            display: none;
            position: absolute;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            background-color: #FFD740;
            opacity: 0.6;
        }

        &.not-free figure::after{
            background-color: $colore-principale;
        }

        &:hover figure::after{
            display: block;
        }
    }
</style>