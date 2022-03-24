<template>
    <header class="container-xl">
        <!-- Per la navbar ho utilizzato il componente di Bootstrap, al quale ho apportato le modifiche necessarie -->
        <nav class="navbar navbar-expand-lg p-0 navbar-dark bg-light">
            <div class="container-fluid px-0 px-lg-2">
                <a class="navbar-brand" href="#">
                    <!-- L'immagine l'ho passata tramite binding dell'elemento data() 'mainLogoLight'  -->
                    <img :src="mainLogoLight" alt="">
                </a>
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse justify-content-end gap-4" id="navbarSupportedContent">
                    <!-- Per la lista dei link della navbar ho utilizzato un ciclo v-for al quale ho passato
                    gli oggetti dell'Array 'navLinks' -->
                    <ul class="navbar-nav me-0 mb-0 flex-grow-1 justify-content-end">
                        <li v-for="(link, index) in navLinks" :key="index" 
                        class="nav-item">
                        <a class="nav-link" :href="link.href">{{ link.link }}</a>
                        </li>
                    </ul>
                    <form class="mt-3 mt-lg-0 d-flex">
                        <a href=""><i class="fa-solid fa-magnifying-glass"></i></a>
                        <a href="">
                            <i class="fa-solid fa-bag-shopping"></i>
                            <div class="cart-number">0</div>
                        </a>
                        <a href=""><i class="fa-solid fa-bars"></i></a>
                    </form>
                </div>
            </div>
        </nav>
    </header>
</template>

<script>

export default {
    name: 'myHeader',

    data(){
        return{
            mainLogoLight: require('../assets/icademy/icademy/img/logo-light.png'),

            navLinks: [
                {
                    href: '#',
                    link: 'home'
                },
                {
                    href: '#',
                    link: 'courses'
                },
                {
                    href: '#',
                    link: 'instructors'
                },
                {
                    href: '#',
                    link: 'events'
                },
                {
                    href: '#',
                    link: 'pages'
                },
                {
                    href: '#',
                    link: 'elements'
                },
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/variables.scss';

    .container-xl{
        padding: 30px 20px;
    }

    .navbar-brand{
        width: 190px;
    }

    a{
        color: white;

        &:hover{
            color: $colore-principale;
        }
    }

    .bg-light {
        --bs-bg-opacity: 0;
    }

    .navbar-dark .navbar-nav .nav-link {
        color: white;
        text-transform: uppercase;

        &:hover{
            color: $colore-principale;
            transition: all 300ms;
        }
    }


    .navbar-nav{
        column-gap: 30px;
        font-weight: 600;
    }

    form{
        column-gap: 35px;
        font-size: 18px;
    }

    form a:nth-child(2n){
        position: relative;

        &:hover .cart-number{
            background-color: white;
            transition: all 300ms;
        }
    }

    .cart-number{
        position: absolute;
        top: -3px;
        right: -8px;
        background-color: $colore-principale;
        width: 16px;
        height: 16px;
        border-radius: 50%;
        font-size: 11px;
        display: flex;
        justify-content: center;
        align-items: center;
    }
</style>