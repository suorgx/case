<script>
import {defineComponent} from 'vue'

export default defineComponent({
    name: "TheChip",
    props: {
        text: String,
        icon: {
            type: String,
            default: 'link'
        }
    }
})
</script>

<template>
    <div class="the-chip">
        <img class="the-chip__icon" :src="`src/assets/images/card_icon_${icon}.svg`" alt=""/>
        <div class="the-chip__name">
            {{ text }}
        </div>
    </div>
</template>

<style lang="scss">
.the-chip {
    border-radius: 5.5px;
    background: $second-color;
    box-shadow: 0 0 6.5px 0 rgba(20, 20, 20, 0.15);
    display: flex;
    padding: 10px;
    justify-content: center;
    align-items: center;
    gap: 10px;
    width: 100%;

    &__icon {
        width: 12px;
        height: 12px;
        display: block;
    }

    &__name {
        color: $base-color;
        font-size: 16px;
        font-weight: 700;
        line-height: 100%;
    }
}
</style>
