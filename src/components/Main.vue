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
        <!-- Sezion 5 del Main  -->
        <onlineCourses />
        <!-- Sezione 6 del Main  -->
        <pricingPlans />
        <!-- Sezione 7 del Main  -->
        <logoSection />
    </main>
</template>

<script>
import coursesSection from './CoursesSection.vue'
import childrenSection from './ChildrenSection.vue'
import studentsCarouselSection from './StudentsCarouselSection.vue'
import learningSection from './LearningSection.vue'
import onlineCourses from './OnlineCourses.vue'
import pricingPlans from './PricingPlans.vue'
import logoSection from './LogoSection.vue'

export default {
    name: 'myMain',

    components: {
        coursesSection,
        childrenSection,
        studentsCarouselSection,
        learningSection,
        onlineCourses,
        pricingPlans,
        logoSection,
    }
}
</script>

<style lang="scss" scoped>

</style>