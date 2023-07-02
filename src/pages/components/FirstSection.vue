<script>
import {defineComponent} from 'vue'
import TheCaption from '@/components/TheCaption.vue'
import TheMainButton from '@/components/TheMainButton.vue'
import TheSearch from '@/components/TheSearch.vue'

export default defineComponent({
    name: "FirstSection",
    components: {
        TheMainButton,
        TheCaption,
        TheSearch
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
                    <TheSearch placeholder="Search by location..." icon></TheSearch>
                </div>
            </div>
            <img class="first-section__right" src="@/assets/images/first_section_image.webp" alt=".">
        </div>
    </section>
</template>

<style lang="scss">
.first-section {
    background: $base-color;
    width: 100%;
    color: $second-color;
    padding-top: 180px;
    padding-bottom: 50px;

    &__wrapper {
        display: flex;
        gap: 40px;
        flex-direction: column;
        align-items: flex-start;
    }

    &__left {
        display: flex;
        flex-direction: column;
        gap: 40px;
        position: relative;
        padding-top: 0;
    }

    &__search {
        position: relative;
        width: 100%;
        bottom: 0;
    }

    &__right {
        max-width: 100%;
        width: 100%;
        display: block;
    }

    &__description {
        color: rgba($second-color, 0.8);
        font-size: 15px;
        font-weight: 500;
        line-height: 110%;
        text-transform: capitalize;
    }

    @media (min-width: $mobile) {
        padding-top: 280px;
        padding-bottom: 80px;
        background: linear-gradient(to right, $base-color 80%, $green-color 80%);

        &__description {
            font-size: 16px;
        }

        &__right {
            max-width: 500px;
        }
    }

    @media (min-width: $tablet) {
        background: linear-gradient(to right, $base-color 61.5%, $green-color 61.5%);
        padding-top: 200px;
        padding-bottom: 100px;

        &__wrapper {
            flex-direction: row;
        }

        &__left {
            gap: 28px;
        }

        &__description {
            font-size: 17px;
        }
    }

    @media (min-width: $laptop) {

        &__wrapper {
            gap: 98px;
        }

        &__right {
            max-width: 603px;
        }

        &__search {
            position: absolute;
            width: 131%;
            bottom: -127px;
        }

        &__description {
            font-size: 18px;
        }

        &__left {
            padding-top: 9px;
        }
    }

}
</style>
