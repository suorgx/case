<script>
import {defineComponent} from 'vue'

export default defineComponent({
    name: "TheMainButton",
    props: {
        text: String,
        size: {
            type: String,
            default: 'l'
        }
    }
})
</script>

<template>
    <button class="the-main-button" :class="`the-main-button--size-${size}`">
        {{ text }}
    </button>
</template>

<style lang="scss">
.the-main-button {
    display: flex;
    align-items: center;
    gap: 10px;
    background: $green-color;
    color: $second-color;
    border: none;
    font-weight: 700;
    line-height: 100%;
    user-select: none;
    cursor: pointer;
    transition: background 0.5s;
    width: fit-content;
    flex-shrink: 0;
    letter-spacing: 1.2px;

    &--size-l {
        padding: 19px 28px;
        font-size: 18px;
        border-radius: 10px;
    }

    &--size-m {
        padding: 13px 26px;
        font-size: 16px;
        border-radius: 10px;
    }

    &--size-s {
        padding: 9px 18px;
        font-size: 14px;
        border-radius: 5px;
    }

    &:hover {
        background: #94B9A9;
    }

    &:active {
        background: #6B7D76;
    }

    &:disabled {
        background: #D3DCD8;
        color: #F5F5F5;
        cursor: auto;
    }

    @media (min-width: $mobile) {
        &--size-l {
            padding: 20px 29px;
            font-size: 19px;
        }

        &--size-m {
            padding: 14px 38px;
            font-size: 17px;
        }

        &--size-s {
            padding: 10px 20px;
            font-size: 15px;
        }
    }

    @media (min-width: $tablet) {
        &--size-l {
            padding: 25px 30px;
            font-size: 20px;
        }

        &--size-m {
            padding: 18px 30px;
            font-size: 18px;
        }

        &--size-s {
            padding: 12px 24px;
            font-size: 16px;
        }
    }
}
</style>
