<script>
import {defineComponent} from 'vue'
import FirstSection from './components/FirstSection.vue'
import SecondSection from './components/SecondSection.vue'

export default defineComponent({
    name: "MainPage",
    components: {
        FirstSection,
        SecondSection
    }
})
</script>

<template>
    <main class="main-page">
        <FirstSection></FirstSection>
        <SecondSection></SecondSection>
    </main>
</template>

<style lang="scss">
.main-page {
    width: 100%;
}
</style>