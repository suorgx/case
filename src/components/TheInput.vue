<script>
import {defineComponent} from 'vue'
import TheMainButton from '@/components/TheMainButton.vue'

export default defineComponent({
    name: "TheInput",
    components: {
        TheMainButton
    },
    props: {
        icon: Boolean,
        placeholder: String
    }
})
</script>

<template>
    <form class="the-input">
        <img v-if="icon" class="the-input__icon" src="@/assets/images/icon_form_location.svg" alt=".">
        <input class="the-input__input" type="text" :placeholder="placeholder"/>
        <TheMainButton text="Search Now"></TheMainButton>
    </form>
</template>

<style lang="scss">
.the-input {
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

    &__input {
        background: transparent;
        width: 100%;
        height: 100%;
        border: none;
        outline: none;
        font-size: 20px;
        font-weight: 400;
        letter-spacing: 0.2px;
        display: block;

        &::placeholder {
            font-size: 20px;
            font-weight: 400;
            color: rgba($base-color, 0.69);
            letter-spacing: 1.2px;
        }

        &:disabled {
            opacity: 0.1;
            pointer-events: none;
        }
    }
}
</style>