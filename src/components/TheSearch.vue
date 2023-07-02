<script>
import {defineComponent} from 'vue'
import TheMainButton from '@/components/TheMainButton.vue'
import TheInput from '@/components/TheInput.vue'

export default defineComponent({
    name: "TheSearch",
    components: {
        TheMainButton,
        TheInput
    },
    props: {
        icon: Boolean,
        placeholder: String
    }
})
</script>

<template>
    <form class="the-search">
        <img v-if="icon" class="the-search__icon" src="@/assets/images/icon_form_location.svg" alt=".">
        <TheInput placeholder="Search by location..."></TheInput>
        <TheMainButton text="Search Now"></TheMainButton>
    </form>
</template>

<style lang="scss">
.the-search {
    border-radius: 10px;
    background: $second-color;
    padding: 10px 10px 10px 24px;
    color: $base-color;
    display: flex;
    align-items: center;
    gap: 10px;
    width: 100%;
    border: 1px solid rgba(125, 155, 143, 0.30);

    &__icon {
        flex-shrink: 0;
        width: 40px;
        height: 40px;
    }
}
</style>