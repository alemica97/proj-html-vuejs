<template>
    <section id="pricing-plans" class="contaer-fluid">
        <div class="circle">
            <figure>
                <img src="../assets/icademy/icademy/svg/svg-0.svg" alt="">
            </figure>
        </div>
        <div class="cart">
            <figure>
                <img src="../assets/icademy/icademy/svg/svg-2.svg" alt="">
            </figure>
        </div>
        <div class="container-sm px-2 px-lg-4">
            <div class="row justify-content-center">
                <div class="col-12 col-md-10 text-center">
                    <h1 class="mb-4">{{ pricingTitle }}</h1>
                    <p class="pricing-par">{{ pricingParagraph }}</p>
                </div>
            </div>
            <div class="table-wrapper">
                <table>
                    <tbody>
                        <tr>
                            <td>
                                <h4>Save up to 40% by paying weekly</h4>
                            </td>
                            <td>
                                <figure class="mb-3">
                                    <img src="../assets/icademy/icademy/img/h5-custom-icon-7.png" alt="">
                                </figure>
                                <h4>Standard</h4>
                                <span>$12</span>
                            </td>
                            <td>
                                <figure class="mb-4">
                                    <img src="../assets/icademy/icademy/img/h5-custom-icon-8.png" alt="">
                                </figure>
                                <h4>Professional</h4>
                                <span>$59</span>
                            </td>
                            <td>
                                <figure class="mb-4">
                                    <img src="../assets/icademy/icademy/img/h5-custom-icon-9.png" alt="">
                                </figure>
                                <h4>Advanced</h4>
                                <span>$88</span>
                            </td>
                        </tr>
                        <tr>
                            <td>
                                <span>Number of Courses</span>
                            </td>
                            <td>
                                <span>2</span>
                            </td>
                            <td>
                                <span>4</span>
                            </td>
                            <td>
                                <span>6</span>
                            </td>
                        </tr>
                        <tr>
                            <td>
                                <span>Time</span>
                            </td>
                            <td>
                                <span>15 Days</span>
                            </td>
                            <td>
                                <span>30 Days</span>
                            </td>
                            <td>
                                <span>30 Days</span>
                            </td>
                        </tr>
                        <tr>
                            <td>
                                <span>Web Designing</span>
                            </td>
                            <td>
                                <span><i class="fa-solid fa-check"></i></span>
                            </td>
                            <td>
                                <span><i class="fa-solid fa-check"></i></span>
                            </td>
                            <td>
                                <span><i class="fa-solid fa-check"></i></span>
                            </td>
                        </tr>
                        <tr>
                            <td>
                                <span>Human-Centered Designing</span>
                            </td>
                            <td>
                                <span><i class="fa-solid fa-check"></i></span>
                            </td>
                            <td>
                                <span><i class="fa-solid fa-check"></i></span>
                            </td>
                            <td>
                                <span><i class="fa-solid fa-check"></i></span>
                            </td>
                        </tr>
                        <tr>
                            <td>
                                <span>Basic Marketing</span>
                            </td>
                            <td>
                                <span><i class="fa-solid fa-xmark"></i></span>
                            </td>
                            <td>
                                <span><i class="fa-solid fa-check"></i></span>
                            </td>
                            <td>
                                <span><i class="fa-solid fa-check"></i></span>
                            </td>
                        </tr>
                        <tr>
                            <td>
                                <span>Pyton for Everybody</span>
                            </td>
                            <td>
                                <span><i class="fa-solid fa-xmark"></i></span>
                            </td>
                            <td>
                                <span><i class="fa-solid fa-check"></i></span>
                            </td>
                            <td>
                                <span><i class="fa-solid fa-check"></i></span>
                            </td>
                        </tr>
                        <tr>
                            <td>
                                <span>Android Developer</span>
                            </td>
                            <td>
                                <span><i class="fa-solid fa-xmark"></i></span>
                            </td>
                            <td>
                                <span><i class="fa-solid fa-xmark"></i></span>
                            </td>
                            <td>
                                <span><i class="fa-solid fa-check"></i></span>
                            </td>
                        </tr>
                        <tr>
                            <td>
                                <span>Business English</span>
                            </td>
                            <td>
                                <span><i class="fa-solid fa-xmark"></i></span>
                            </td>
                            <td>
                                <span><i class="fa-solid fa-xmark"></i></span>
                            </td>
                            <td>
                                <span><i class="fa-solid fa-check"></i></span>
                            </td>
                        </tr>
                        <tr>
                            <td>
                                <span></span>
                            </td>
                            <td>
                                <button class="btn-white">get it now</button>
                            </td>
                            <td>
                                <button class="btn-blue">get it now</button>
                            </td>
                            <td>
                                <button class="btn-white">get it now</button>
                            </td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
        
    </section>
</template>

<script>
export default {
    name: 'pricingPlans',

    data(){
        return{
            pricingTitle: 'Pricing Plans',
            pricingParagraph: `Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
                              sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.`,
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/variables.scss';

    #pricing-plans{
        padding: 140px 0;
        background-image: url(../assets/icademy/icademy/img/background-pattern.jpg);
        background-position: 50% 30%;
        position: relative;
        border-bottom: 1px solid $section-border;

        .circle, .cart{
            width: 50px;
            height: 50px;
            padding: 8px;
            box-shadow: 0 0 10px 0 #ABABAB;
            margin: 15px 0;
            position: sticky;

            &:hover img{
                transform: scale(1.1, 1.1);
                cursor: pointer;
                transition: all 300ms;
            }
        }

        .circle{
            background-color: #EE2852;
            top: 60px;
        }
        .cart{
            background-color: white;
            top: 125px;
        }
    }

    h1{
        font-size: $main-title;
        font-weight: 700;
        color: $title-dark;
    }

    .pricing-par{
        font-size: $main-par;
        color: $par-dark;
        margin-bottom: 100px;
    }

    .table-wrapper{
        overflow-x: auto;
    }

    ::-webkit-scrollbar {
            height: 15px;
        }

        ::-webkit-scrollbar-track{
            background-color: rgba(51, 51, 51, 0.7);
            border-radius: 100px;
            margin-right: 0;
        }

        ::-webkit-scrollbar-thumb{
            background-color: $colore-principale;
            border-radius: 100px;
        }

        ::-webkit-scrollbar-thumb:hover{
            background-color: #34a2d4;
        }

    table{
        width: 100%;
        tr{
            width: 100%;
        }
    }

    td{
        text-align: center;
        padding: 30px 0;
        width: calc(100% / 4);
        border: 1px solid $column-border;
        font-size: calc(16px + 0.4vw);
        font-weight: 700;
        color: #847B7B;
        background-color: white;

        h4{
            font-size: calc(22px + 0.3vw);
            font-weight: 700;
            color: #3E3E3E;
        }

        .fa-check{
            color: $colore-principale;
        }
    }

    table tr:first-child{
        td{
            padding: 35px 25px;
            border-top: 5px solid #D6F2FF;

            &:nth-child(3n){
                border-top: 5px solid $colore-principale;
            }
            
        }

        td span{
            color:#595959;
        }

        & td:nth-child(1n + 2){
            background-color: $table-bkc;
        }
    }

    table tr:last-child{
        td{
            padding: 25px 0;
        }
        & td:nth-child(1n + 2){
            background-color: $table-bkc;
        }
    }

    button{
        font-size: 15px;
        padding: 15px 35px;
    }
</style>