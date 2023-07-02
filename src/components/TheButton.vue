<script>
import {defineComponent} from 'vue'

export default defineComponent({
    name: "TheButton",
    props: {
        text: String
    }
})
</script>

<template>
    <button class="the-button">
        {{ text }}
    </button>
</template>

<style lang="scss">
.the-button {
    display: flex;
    padding: 13px 26px;
    align-items: center;
    gap: 10px;
    border-radius: 5px;
    background: $second-color;
    color: $base-color;
    border: none;
    font-size: 16px;
    font-weight: 500;
    line-height: 100%;
    user-select: none;
    cursor: pointer;
    transition: background 0.5s;
    width: fit-content;
    flex-shrink: 0;
    letter-spacing: 2px;

    &:hover {
        background: #E9FFF6;
    }

    &:active {
        background: #CCD7D2;
    }

    &:disabled {
        background: #D3D4D4;
        color: rgba(255, 255, 255, 0.60);
        cursor: auto;
    }

    @media (min-width: $mobile) {
        padding: 16px 28px;
        font-size: 18px;
    }

    @media (min-width: $tablet) {
        padding: 20px 30px;
        font-size: 20px;
    }
}
</style>
