<script>
import {defineComponent} from 'vue'
import TheChip from '@/components/TheChip.vue'

export default defineComponent({
    name: "TheCard",
    components: {
        TheChip
    }
})
</script>

<template>
    <div class="the-card">
        <img class="the-card__image" src="@/assets/images/card_image.webp" alt=".">
        <div class="the-card__info">
            <div class="the-card__price">
                $ 59,345
            </div>
            <div class="the-card__name">
                Lorem ipsum dolor sit
            </div>
            <div class="the-card__divider"></div>
            <div class="the-card__chips">
                <TheChip text="2500 sqft"></TheChip>
                <TheChip text="3" icon="bed"></TheChip>
                <TheChip text="2" icon="bath"></TheChip>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
.the-card {
    width: 100%;
    border-radius: 10px;
    overflow: hidden;
    background: $second-color;

    &__image {
        width: 100%;
        height: 280px;
        display: block;
        object-fit: cover;
    }

    &__info {
        padding: 32px;
        display: flex;
        flex-direction: column;
        gap: 22px;
    }

    &__divider {
        width: 100%;
        height: 1px;
        flex-shrink: 0;
        background: $base-color;
    }

    &__price {
        color: $base-color;
        font-size: 24px;
        font-weight: 700;
        line-height: 100%;
    }

    &__name {
        color: $base-color;
        font-size: 20px;
        font-weight: 700;
    }

    &__chips {
        display: grid;
        grid-template-columns: 2fr 1fr 1fr;
        gap: 10px;
        align-items: center;
    }
}
</style>
