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
        <div class="the-search__wrapper">
            <img v-if="icon" class="the-search__icon" src="@/assets/images/icon_form_location.svg" alt=".">
            <TheInput placeholder="Search by location..."></TheInput>
            <TheMainButton class="hide--default show--laptop" text="Search Now"></TheMainButton>
        </div>
        <TheMainButton class="the-search__submit hide--laptop show--default" text="Search Now"></TheMainButton>
    </form>
</template>

<style lang="scss">
.the-search {

    &__wrapper {
        border-radius: 10px;
        background: $second-color;
        padding: 5px 5px 5px 12px;
        color: $base-color;
        display: flex;
        align-items: center;
        gap: 5px;
        width: 100%;
        border: 1px solid rgba(125, 155, 143, 0.30);
        margin-bottom: 10px;
    }

    &__icon {
        flex-shrink: 0;
        width: 40px;
        height: 40px;
    }

    &__submit {
        margin: 0;
    }

    @media (min-width: $mobile) {
        &__wrapper {
            margin-bottom: 12px;
            padding: 10px 10px 10px 24px;
            gap: 10px;
        }
    }

    @media (min-width: $laptop) {
        &__wrapper {
            margin-bottom: 0;
        }
    }
}
</style>