<script>
import {defineComponent} from 'vue'

export default defineComponent({
    name: "TheCaption",
    props: {
        text: String,
        baseColor: {
            type: Boolean,
            default: false
        },
        tag: {
            type: String,
            default: "h2"
        },
        font: {
            type: String,
            default: 'base'
        }
    }
})
</script>
<template>
    <component
        :is="tag"
        :class="[
        'the-caption',
        {'the-caption--base-color': baseColor},
        {'the-caption--second-color': !baseColor},
        `the-caption--${tag}`,
        `the-caption--${font}-font`
        ]"
    >
        {{ text }}
    </component>
</template>

<style lang="scss">
.the-caption {
    color: $second-color;
    font-size: 58px;
    font-weight: 700;

    &--h1 {
        font-size: 58px;
    }

    &--h2 {
        font-size: 50px;
    }

    &--h3 {
        font-size: 45px;
    }

    &--base-font {
        font-family: $base-font;
    }

    &--second-font {
        font-family: $second-font;
    }

    &--third-font {
        font-family: $third-font;
        letter-spacing: 0.6px;
    }

    &--base-color {
        color: $base-color;
    }

    &--second-color {
        color: $second-color;
    }
}
</style>
