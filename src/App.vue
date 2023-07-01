<script>
import {defineComponent} from 'vue'
import TheHeader from './components/TheHeader.vue'
import TheFooter from './components/TheFooter.vue'
import MainPage from './pages/MainPage.vue'

export default defineComponent({
    name: "App",
    components: {
        TheHeader,
        TheFooter,
        MainPage
    }
})
</script>

<template>
    <TheHeader></TheHeader>
    <MainPage></MainPage>
    <TheFooter></TheFooter>
</template>

<style lang="scss">

</style>