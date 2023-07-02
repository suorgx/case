<script>
import {defineComponent} from 'vue'
import TheMainButton from '@/components/TheMainButton.vue'

export default defineComponent({
    name: "TheSlide",
    components: {
        TheMainButton
    },
    props: {
        date: String,
        img: String,
        title: String
    }
})
</script>

<template>
    <div class="the-slide">
        <img
            v-if="img"
            class="the-slide__img"
            :src="`src/assets/images/${img}`"
            alt="."
        >
        <div v-if="date" class="the-slide__date">
            {{ date }}
        </div>
        <div v-if="date" class="the-slide__divider"></div>
        <h4 v-if="title" class="the-slide__title">
            {{ title }}
        </h4>
        <TheMainButton text="Read More" size="s"></TheMainButton>
    </div>
</template>

<style lang="scss">
.the-slide {
    width: 100%;

    &__img {
        display: block;
        width: 100%;
        max-height: 268px;
        height: 100%;
        object-fit: cover;
        margin-bottom: 30px;
    }

    &__date {
        color: rgba($base-color, 0.69);
        font-size: 14px;
        font-weight: 700;
        line-height: 110%;
        margin-bottom: 8px;
    }

    &__divider {
        max-width: 144px;
        width: 100%;
        height: 1px;
        opacity: 0.699999988079071;
        background: rgba($base-color, 0.69);
        margin-bottom: 16px;
    }

    &__title {
        color: $base-color;
        width: 91%;
        font-size: 24px;
        font-weight: 700;
        line-height: 110%;
        margin-bottom: 21px;
    }
}
</style>