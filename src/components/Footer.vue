<template>
    <footer id="footer" class="container-fluid">
        <div class="container-sm">
            <div class="row py-5">
                <div class="col-6 col-md-3 g-5">
                    <figure class="logo mb-4">
                        <img :src="footerLinks1[0]" alt="">
                    </figure>
                    <p class="mb-4">{{ footerLinks1[1] }}</p>
                    <span class="d-block mb-3 phone-clock">
                        <i class="fas fa-phone-alt"></i>
                        {{ footerLinks1[2] }}
                    </span>
                    <span class="phone-clock">
                        <i class="far fa-clock"></i>
                        {{ footerLinks1[3] }}
                    </span>
                </div>
                <div class="col-6 col-md-3 g-5">
                    <h3 class="footer-title mb-4">
                        {{ footerLinks2[0] }}
                    </h3>
                    <div class="pop-courses"
                    v-for="(el, i) in footerLinks2[1]" :key="i">
                        <h4 class="mb-0 mt-4">
                            <a href="">{{ el.subtitle }}</a>
                        </h4>
                        <span class="">{{ el.teacher }}</span>
                    </div>
                </div>
                <div class="col-6 col-md-3 g-5">
                    <h3 class="footer-title mb-4">
                        {{ footerLinks3[0] }}
                    </h3>
                    <p class="footer-par" 
                    v-for="(el, i) in footerLinks3[1]" :key="i">
                        <a href="">{{ el }}</a>
                    </p>
                </div>
                <div class="col-6 col-md-3 g-5">
                    <h3 class="footer-title mb-4">
                        {{ footerLinks4[0] }}
                    </h3>
                    <figure>
                        <img :src="footerLinks4[1]" alt="">
                    </figure>
                </div>
            </div>
        </div>
        <div class="container-sm">
            <div class="row align-items-center py-3">
                <div class="col-12 col-md-4 col-lg-5 col-xxl-7">
                    <span>{{copy}}</span>
                </div>
                <div class="col-12 col-md-8 col-lg-7 col-xxl-5 d-flex justify-content-around">
                    <span>{{phone}}</span>
                    <span>{{follow}}</span>
                    <span><i class="fab fa-twitter"></i></span>
                    <span><i class="fab fa-instagram"></i></span>
                    <span><i class="fab fa-facebook-f"></i></span>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'myFooter',

    data(){
        return{
            footerLinks1: [
                require('../assets/icademy/icademy/img/logo-light.png'),
                `Providing Life Changing Experiences Through Education. 
                Class That Fit Your Busy Life. Closer to Home.`,
                '1-677-124-44227',
                'Mon-Sat 8.00 - 18.00'
            ],
            footerLinks2: [
                'Popular Courses',
                [
                    {
                        subtitle: 'Business English',
                        teacher: 'Preston Marshall'
                    },
                    {
                        subtitle: 'Social Computing',
                        teacher: 'David Sanders'
                    },
                    {
                        subtitle: 'Learn Spanish',
                        teacher: 'Jennie King'
                    }
                ],
            ],
            footerLinks3: [
                'Support',
                [
                    'User dashboard',
                    'Contact Us',
                    'FAQ',
                    'Course Offer',
                    'Events'
                ],
            ],

            footerLinks4: [
                'Flexible Learning',
                require('../assets/icademy/icademy/img/footer-img-1.png')
            ],

            copy: 'Copyrights 2017 ©️Mikado Themes',
            phone: 'CALL +44 300 303 0266',
            follow: 'FOLLOW US',
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/variables.scss';

    #footer{
        background-color: #222222;
        color: #B9B9B9;

        .container-sm:first-child{
            border-bottom: 1px solid #efefef62;
        }

        .container-sm:last-child{
            span{
                font-size: calc(12px + 0.2vw);
            }
        }

        h3{
            color: white;
        }
    }

    .logo{
        width: 140px;
    }

    i{
        margin-right: 8px;
    }

    .footer-title{
        font-size: calc(20px + 0.4vw);
        font-weight: 700;
    }

    .phone-clock{
        color: #CECECE;
        font-weight: 700;
    }

    .pop-courses{

        h4{
            font-size: calc(15px + 0.3vw);
            a{
                color: #C6C6C6;
                    &:hover{
                    color: #55ACEE;
                    transition: all 500ms;
                }
            }
        }
        span{
            font-size: calc(14px + 0.1vw);
        }
    }

    .footer-par{
        a{
            color: currentColor;
            &:hover{
                color: #3DB3E8;
                transition: all 500ms;
            }
        }
    }

    @media screen and (max-width: 992px){
        [class*='col-']{
            padding: 20px 10px 20px 10px;
        }
    }

    @media screen and (min-width: 993px){
        [class*='col-']{
            padding: 20px 60px 20px 20px;
        }
    }
</style>