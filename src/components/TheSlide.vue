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
        <div v-if="title" class="the-slide__title">
            {{ title }}
        </div>
        <TheMainButton text="read more" size="s"></TheMainButton>
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
}
</style>