<template>
    <main>
        <!-- Sezione 1 del Main  -->
        <coursesSection />
        <!-- Sezione 2 del Main  -->
        <childrenSection />
        <!-- Sezione 3 del Main  -->
        <studentsCarouselSection />
        <!-- Sezione 4 del Main  -->
        <learningSection />
    </main>
</template>

<script>
import coursesSection from './CoursesSection.vue'
import childrenSection from './ChildrenSection.vue'
import studentsCarouselSection from './StudentsCarouselSection.vue'
import learningSection from './LearningSection.vue'

export default {
    name: 'myMain',

    components: {
        coursesSection,
        childrenSection,
        studentsCarouselSection,
        learningSection,
    }
}
</script>

<style lang="scss" scoped>

</style>