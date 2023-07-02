<script>
import {defineComponent} from 'vue'
import FirstSection from './components/FirstSection.vue'
import SecondSection from './components/SecondSection.vue'
import ThirdSection from '@/pages/components/ThirdSection.vue'
import FourthSection from '@/pages/components/FourthSection.vue'
import FifthSection from '@/pages/components/FifthSection.vue'

export default defineComponent({
    name: "MainPage",
    components: {
        FirstSection,
        SecondSection,
        ThirdSection,
        FourthSection,
        FifthSection
    }
})
</script>

<template>
    <main class="main-page">
        <FirstSection></FirstSection>
        <SecondSection></SecondSection>
        <ThirdSection></ThirdSection>
        <FourthSection></FourthSection>
        <FifthSection></FifthSection>
    </main>
</template>

<style lang="scss">
.main-page {
    width: 100%;
}
</style>