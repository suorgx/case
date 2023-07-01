<script>
import {defineComponent} from 'vue'
import FirstSection from './components/FirstSection.vue'
import SecondSection from './components/SecondSection.vue'
import ThirdSection from '@/pages/components/ThirdSection.vue'

export default defineComponent({
    name: "MainPage",
    components: {
        FirstSection,
        SecondSection,
        ThirdSection
    }
})
</script>

<template>
    <main class="main-page">
        <FirstSection></FirstSection>
        <SecondSection></SecondSection>
        <ThirdSection></ThirdSection>
    </main>
</template>

<style lang="scss">
.main-page {
    width: 100%;
}
</style>