<script>
import {defineComponent} from 'vue'
import TheLogo from '@/components/TheLogo.vue'
import TheNav from '@/components/TheNav.vue'
import TheButton from '@/components/TheButton.vue'

export default defineComponent({
    name: "TheHeader",
    components: {
        TheLogo,
        TheNav,
        TheButton
    }
})
</script>

<template>
    <header class="the-header container">
        <TheLogo></TheLogo>
        <TheNav></TheNav>
        <TheButton @click="$emit('openModal')" text="Contact"></TheButton>
    </header>
</template>

<style lang="scss">
.the-header {
    padding-top: 20px;
    padding-bottom: 20px;
    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: space-between;
    position: absolute;
    background: transparent;
    gap: 10px;

    @media (min-width: $mobile) {
        padding-top: 40px;
        padding-bottom: 40px;
        gap: 20px;
    }

    @media (min-width: $tablet) {
        padding-top: 40px;
        padding-bottom: 40px;
        flex-direction: row;
    }
}
</style>
