<script>
import {defineComponent} from 'vue'

export default defineComponent({
    name: "TheTextarea",
    props: {
        placeholder: String
    }
})
</script>

<template>
    <textarea class="the-textarea"
              rows="7"
              :placeholder="placeholder"
    />
</template>

<style lang="scss">
.the-textarea {
    background: transparent;
    width: 100%;
    height: 100%;
    outline: none;
    font-size: 16px;
    font-weight: 400;
    letter-spacing: 0.2px;
    display: block;
    border-radius: 5px;
    border: 1px solid rgba($green-color, 0.30);
    background: $second-color;
    padding: 8px;
    resize: none;

    &::placeholder {
        font-size: 16px;
        font-family: $base-font;
        font-weight: 400;
        color: rgba($base-color, 0.5);
        letter-spacing: 0.2px;
    }

    &:disabled {
        opacity: 0.1;
        pointer-events: none;
    }

    @media (min-width: $mobile) {
        font-size: 20px;
        padding: 16px;

        &::placeholder {
            font-size: 20px;
        }
    }
}
</style>