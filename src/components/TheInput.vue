<script>
import {defineComponent} from 'vue'

export default defineComponent({
    name: "TheInput",
    props: {
        placeholder: String,
        required: Boolean,
        border: Boolean,
        type: {
            type: String,
            default: 'text'
        }
    }
})
</script>

<template>
    <input :class="['the-input', {'the-input--border': border}]"
           :type="type"
           :placeholder="placeholder"
           :required="required"
    />
</template>

<style lang="scss">
.the-input {
    background: transparent;
    width: 100%;
    height: 100%;
    border: none;
    outline: none;
    font-size: 16px;
    font-weight: 400;
    letter-spacing: 0.2px;
    display: block;

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

    &--border {
        border-radius: 5px;
        border: 1px solid rgba($green-color, 0.30);
        background: $second-color;
        padding: 8px;
    }

    @media (min-width: $mobile) {
        font-size: 20px;

        &::placeholder {
            font-size: 20px;
        }

        &--border {
            padding: 16px;
        }
    }
}
</style>