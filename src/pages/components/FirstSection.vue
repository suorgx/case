<script>
import {defineComponent} from 'vue'
import TheCaption from '@/components/TheCaption.vue'
import TheMainButton from '@/components/TheMainButton.vue'
import TheInput from '@/components/TheInput.vue'

export default defineComponent({
    name: "FirstSection",
    components: {
        TheMainButton,
        TheCaption,
        TheInput
    }
})
</script>

<template>
    <section class="first-section">
        <div class="container first-section__wrapper">
            <div class="first-section__left">
                <TheCaption tag="h1" text="Lectus Magna Fringilla Urna, Porttitor"></TheCaption>
                <p class="first-section__description">
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit ut&nbsp;aliquam, purus sit amet luctus
                    venenatis, lectus magna fringilla urna, porttitor.
                </p>
                <div class="first-section__search">
                    <TheInput placeholder="Search by location..." icon></TheInput>
                </div>
            </div>
            <img class="first-section__right" src="@/assets/images/first_section_image.webp" alt=".">
        </div>
    </section>
</template>

<style lang="scss">
.first-section {
    background: linear-gradient(to right, $base-color 61.5%, $green-color 61.5%);
    width: 100%;
    color: $second-color;
    padding-top: 200px;
    padding-bottom: 100px;

    &__wrapper {
        display: flex;
        gap: 98px;
        flex-direction: row;
        align-items: flex-start;
    }

    &__left {
        display: flex;
        flex-direction: column;
        gap: 28px;
        position: relative;
        padding-top: 9px;
    }

    &__search {
        position: absolute;
        width: 131%;
        bottom: -127px;
    }

    &__right {
        max-width: 603px;
        width: 100%;
        display: block;
    }

    &__description {
        color: rgba($second-color, 0.8);
        font-size: 18px;
        font-weight: 500;
        line-height: 110%;
        text-transform: capitalize;
    }

}
</style>
