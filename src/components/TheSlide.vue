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
        <img v-if="img === '1'" class="the-slide__img" src="@/assets/images/slide_image_1.webp" alt=".">
        <img v-if="img === '2'" class="the-slide__img" src="@/assets/images/slide_image_2.webp" alt=".">
        <img v-if="img === '3'" class="the-slide__img" src="@/assets/images/slide_image_3.webp" alt=".">
        <div v-if="date" class="the-slide__date">
            {{ date }}
        </div>
        <div v-if="date" class="the-slide__divider"></div>
        <p v-if="title" class="the-slide__title">
            {{ title }}
        </p>
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
        margin-bottom: 10px;
    }

    &__date {
        color: rgba($base-color, 0.69);
        font-size: 11px;
        font-weight: 700;
        line-height: 110%;
        margin-bottom: 6px;
    }

    &__divider {
        max-width: 144px;
        width: 100%;
        height: 1px;
        opacity: 0.699999988079071;
        background: rgba($base-color, 0.69);
        margin-bottom: 8px;
    }

    &__title {
        color: $base-color;
        width: 91%;
        font-size: 16px;
        font-weight: 700;
        line-height: 110%;
        margin-bottom: 12px;
    }

    @media (min-width: $mobile) {
        &__img {
            margin-bottom: 20px;
        }

        &__date {
            font-size: 12px;
        }

        &__title {
            font-size: 20px;
            margin-bottom: 16px;
        }
    }

    @media (min-width: $tablet) {
        &__img {
            margin-bottom: 30px;
        }

        &__date {
            font-size: 14px;
            margin-bottom: 8px;
        }

        &__divider {
            margin-bottom: 16px;
        }

        &__title {
            font-size: 24px;
            margin-bottom: 21px;
        }
    }
}
</style>