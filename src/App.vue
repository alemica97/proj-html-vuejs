<template>
    <div id="app">
        <myJumbo />
        <myMain />
        <myFooter />
    </div>
</template>

<script>
import myJumbo from './components/Jumbo.vue'
import myMain from './components/Main.vue'
import myFooter from './components/Footer.vue'

export default {
    name: 'App',

    components: {
        myJumbo,
        myMain,
        myFooter,
    }
}
</script>

<style lang="scss">
@import '~@fortawesome/fontawesome-free/css/all.css';
@import './assets/scss/common.scss';


</style>
