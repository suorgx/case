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
        `the-caption--${tag}`
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

    &--h2 {
        font-size: 58px;
    }

    &--h3 {
        font-size: 50px;
    }

    &--base-color {
        color: $base-color;
    }

    &--second-color {
        color: $second-color;
    }
}
</style>
