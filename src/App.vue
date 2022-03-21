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
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
