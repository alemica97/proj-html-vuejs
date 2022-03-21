<template>
    <div>
        <myHeader />
    </div>
</template>

<script>
import myHeader from './Header.vue'

export default {
    name: 'myJumbo',

    components: {
        myHeader,
    }
}
</script>

<style lang="scss" scoped>
    div{
        background-color: #333;
    }
</style>