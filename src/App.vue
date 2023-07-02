<script>
import {defineComponent} from 'vue'
import TheHeader from './components/TheHeader.vue'
import TheFooter from './components/TheFooter.vue'
import MainPage from './pages/MainPage.vue'
import TheModal from './components/TheModal.vue'

export default defineComponent({
    name: "App",
    components: {
        TheHeader,
        TheFooter,
        MainPage,
        TheModal
    },
    data() {
        return {
            modal: false
        };
    },
    methods: {
        openModal () {
            this.modal = true
        },
        closeModal () {
            this.modal = false
        }
    }
})
</script>

<template>
    <TheHeader @open-modal="openModal"></TheHeader>
    <MainPage></MainPage>
    <TheFooter></TheFooter>
    <TheModal :is-visible="modal" @close-modal="closeModal"></TheModal>
</template>

<style lang="scss">

</style>