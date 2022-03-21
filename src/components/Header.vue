<template>
    <header class="container-md p-3">
        <!-- Per la navbar ho utilizzato il componente di Bootstrap, al quale ho apportato le modifiche necessarie -->
        <nav class="navbar navbar-expand-lg p-0 navbar-dark bg-light">
            <div class="container-fluid">
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
                    <ul class="navbar-nav me-0 mb-0 gap-3">
                        <li v-for="(link, index) in navLinks" :key="index" 
                        class="nav-item">
                        <a class="nav-link" :href="link.href">{{ link.link }}</a>
                        </li>
                    </ul>
                    <form class="d-flex gap-4">
                        <a href=""><i class="fa-solid fa-magnifying-glass"></i></a>
                        <a href=""><i class="fa-solid fa-bag-shopping"></i></a>
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

    .navbar-brand{
        width: 150px;
    }

    a{
        color: white;
        text-decoration: none;

        &:hover{
            color: #55ACEE;
        }
    }

    .bg-light {
        --bs-bg-opacity: 0;
    }

    .navbar-dark .navbar-nav .nav-link {
        color: white;
        text-transform: uppercase;

        &:hover{
            color: #55ACEE;
        }
    }

</style>