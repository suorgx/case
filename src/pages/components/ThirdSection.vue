<script>
import {defineComponent} from 'vue'
import TheCaption from '@/components/TheCaption.vue'
import TheAccordion from '@/components/TheAccordion.vue'

export default defineComponent({
    name: "ThirdSection",
    components: {
        TheAccordion,
        TheCaption
    }
})
</script>

<template>
    <section class="third-section">
        <div class="container third-section__wrapper">
            <img
                class="third-section__left"
                src="@/assets/images/third_section_image_small.webp"
                srcset="@/assets/images/third_section_image_small.webp 500w,
                        @/assets/images/third_section_image_medium.webp 1000w,
                        @/assets/images/third_section_image_large.webp 1500w"
                alt="."
            />
            <div class="third-section__right">
                <TheCaption text="Purus Sit Amet Luctus" base-color></TheCaption>
                <p class="third-section__description">
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit ut&nbsp;aliquam, purus sit amet luctus venenatis, lectus magna.
                </p>
                <div class="third-section__accordion">
                    <TheAccordion></TheAccordion>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
.third-section {
    width: 100%;
    color: $base-color;
    padding-top: 50px;
    padding-bottom: 25px;

    &__wrapper {
        display: flex;
        gap: 40px;
        flex-direction: column-reverse;
        align-items: flex-start;
    }

    &__left {
        max-width: 100%;
        max-height: 300px;
        object-fit: cover;
        width: 100%;
        flex-shrink: 0;
        display: block;
    }

    &__right {
        padding-top: 0;
        display: flex;
        flex-direction: column;
        gap: 40px;
    }

    &__description {
        color: $base-color;
        font-size: 16px;
        font-style: normal;
        font-weight: 500;
        line-height: 150%;
        text-transform: capitalize;
        width: 92%;
    }

    &__accordion {
        margin-top: 0;
    }

    @media (min-width: $mobile) {
        padding-top: 100px;
        padding-bottom: 50px;

        &__description {
            font-size: 18px;
        }

        &__right {
            gap: 17px;
        }

        &__left {
            max-width: 460px;
            max-height: 728px;
        }
    }

    @media (min-width: $tablet) {
        padding-top: 140px;
        padding-bottom: 70px;

        &__wrapper {
            flex-direction: row;
        }

        &__description {
            font-size: 19px;
        }
    }

    @media (min-width: $laptop) {
        padding-top: 150px;
        padding-bottom: 75px;

        &__wrapper {
            gap: 80px;
        }

        &__left {
            max-width: 572px;
        }

        &__right {
            padding-top: 12px;
        }

        &__description {
            font-size: 20px;
        }

        &__accordion {
            margin-top: 26px;
        }
    }
}
</style>
