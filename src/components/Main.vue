<template>
    <main>
        <!-- Sezione 1 del Main  -->
        <coursesSection />
        <!-- Sezione 2 del Main  -->
        <childrenSection />
    </main>
</template>

<script>
import coursesSection from './CoursesSection.vue'
import childrenSection from './ChildrenSection.vue'

export default {
    name: 'myMain',

    components: {
        coursesSection,
        childrenSection,
    }
}
</script>

<style lang="scss" scoped>

</style>