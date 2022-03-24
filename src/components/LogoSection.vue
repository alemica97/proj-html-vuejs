<template>
    <section id="logo-section" class="container-fluid">
        <div class="container-sm">
            <div class="row justify-content-center">
            <div class="col-12 col-md-6 col-lg-3 g-4 d-flex justify-content-center"
            v-for="(image, i) in logoArray"
            :key="i">
                <figure>
                    <img :src="image" alt="">
                    <img :src="logoHoverArray[i]" alt="">
                </figure>
            </div> 
        </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'logoSection',

    data(){
        return{
            check: true,

            logoArray: [
                require('../assets/icademy/icademy/img/h5-client-5.png'),
                require('../assets/icademy/icademy/img/h5-client-1.png'),
                require('../assets/icademy/icademy/img/h5-client-2.png'),
                require('../assets/icademy/icademy/img/h5-client-3.png')
            ],
            logoHoverArray: [
                require('../assets/icademy/icademy/img/h5-client-5-h.png'),
                require('../assets/icademy/icademy/img/h5-client-1-h.png'),
                require('../assets/icademy/icademy/img/h5-client-2-h.png'),
                require('../assets/icademy/icademy/img/h5-client-3-h.png')
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
    #logo-section{
        padding: 60px 0 80px 0;
    }

    figure{
        width: 200px;
        &:hover{
            cursor: pointer;
            & img:last-child{
                display: block;
                transform: scale(1.1, 1.1);
                transition: all 500ms;
            }
            & img:first-child{
                display: none;
            }
        }

        & img:last-child{
            display: none;
        }
    }
</style>