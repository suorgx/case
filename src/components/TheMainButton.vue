<script>
import {defineComponent} from 'vue'

export default defineComponent({
    name: "TheMainButton",
    props: {
        text: String
    }
})
</script>

<template>
    <button class="the-main-button">
        {{ text }}
    </button>
</template>

<style lang="scss">
.the-main-button {
    display: flex;
    padding: 25px 30px;
    align-items: center;
    gap: 10px;
    border-radius: 10px;
    background: $green-color;
    color: $second-color;
    border: none;
    font-size: 20px;
    font-weight: 700;
    line-height: 100%;
    user-select: none;
    cursor: pointer;
    transition: background 0.5s;
    width: fit-content;
    flex-shrink: 0;
    letter-spacing: 1.2px;

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
}
</style>
