<template>
    <div class="col-9 col-md-4">
        <div class="card-wrapper">
            <figure>
            <img :src="singleCard.image" alt="">
            </figure>
            <div class="card-info">
                <div class="teacher">
                    <span>{{singleCard.title}}</span>
                    <span>{{singleCard.name}}</span>
                </div>
                <div class="card-price"
                :class="isFree() ? '' : 'not-free'">
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
                color: black;
                white-space: nowrap;
            }
        }

        .card-price{
            width: 55px;
            height: 24px;
            text-align: center;
            line-height: 26px;
            font-size: 14px;
            color: #ffffff;
            background-color: #FFD740;
            font-weight: 700;
            border-radius: 20px;

            &.not-free{
                background-color: #40C4FF;
            }
        }
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
        span{
            margin-right: 20px;
        }
        i{
            margin-right: 8px;
        }
    }

    .card-wrapper{
        color: #B9B9B9;
        border: 1px solid #B9B9B9;
    }
</style>