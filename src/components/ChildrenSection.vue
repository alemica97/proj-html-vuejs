<template>
    <section id="children-potential" class="container-fluid">
        <div class="container-sm px-0 px-lg-4">
            <!-- divido la sezione con una riga suddivisa in due colonne della stessa larghezza  -->
            <div class="row align-items-center flex-column-reverse flex-md-row py-5">
               
                <div class="col-12 col-md-6">
                    <figure class="text-center">
                        <img :src="childrenPotentialImg" alt="">
                    </figure>
               
                </div>
                <div class="col-12 col-md-6">
                    <!-- nella colonna di destra inserisco un'altra roe che suddivido in due col-12 e due col-6  -->
                    <div class="children-potential-description row mb-5 mb-md-0">
                        <div class="col-12 mb-3">
                            <h1>{{ childrenPotentialTitle }}</h1>
                        </div>
                        <div class="col-12 mb-3">
                            <p>{{ childrenPotentialParagraph }}</p>
                        </div>
                        <div class="children-potential-number col-6">
                            <h2>168</h2>
                            <span>User Stories</span>
                        </div>
                        <div class="children-potential-number col-6">
                            <h2>347</h2>
                            <span>Events</span>
                        </div>
                    </div>
                    
                </div>
            </div>
        </div>
    </section>
</template>

<script>

export default {
    name: 'childrenSection',

    data(){
        return{
            childrenPotentialImg: require('../assets/icademy/icademy/img/h5-img-2.jpg'),
            childrenPotentialTitle: 'Empowering Children to Reach Their Potential.',
            childrenPotentialParagraph: `Lorem ipsum dolor sit amet, consectetur adipisicing.
                                        Hic, quia facere magnam assumenda perspiciatis obcaecati.
                                        Facere ipsa natus fuga ipsum ad odio.
                                        Quasi aut provident mollitia. Nam, tempore laborum?`,
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/variables.scss';

    .container-sm{
        padding: 80px 0 20px 0;
    }
    .children-potential-description{

        h1{
            font-size: $main-title;
            font-weight: 600;
            color: $title-dark;
        }
         
        p{
             font-size: $main-par;
             color: $par-dark;
         }
    }

    .children-potential-number{
        color: $colore-principale;

        h2{
            font-weight: 700;
            font-size: 55px;
            margin-bottom: 0;
        }

        span{
            font-size: 20px;
            font-weight: 700;
        }
    }

</style>