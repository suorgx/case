<script>
import {defineComponent} from 'vue'
import TheCaption from '@/components/TheCaption.vue'
import TheCard from '@/components/TheCard.vue'
import TheQuote from '@/components/TheQuote.vue'

export default defineComponent({
    name: "SecondSection",
    components: {
        TheCaption,
        TheCard,
        TheQuote
    }
})
</script>

<template>
    <section class="second-section">
        <div class="container">
            <div class="second-section__wrapper">
                <div class="second-section__head">
                    <TheCaption text="lectus magna" base-color></TheCaption>
                    <a class="second-section__link" href="#">
                        Explore All
                    </a>
                </div>
                <div class="second-section__main">
                    <div class="second-section__cards">
                        <TheCard></TheCard>
                        <TheCard></TheCard>
                        <TheCard></TheCard>
                    </div>
                    <TheQuote
                        name="John Doe"
                        position="Founder HyperEstate"
                        quote="Lorem ipsum dolor sit amet, consectetur adipiscing elit ut&nbsp;aliquam, purus sit amet luctus venenatis, lectus magna fringilla urna, porttitor."
                    ></TheQuote>
                </div>
                <div class="second-section__divider"></div>
                <div class="second-section__partners">
                    <img class="second-section__partner" src="@/assets/images/partner_logo_1.webp" alt=".">
                    <img class="second-section__partner" src="@/assets/images/partner_logo_2.webp" alt=".">
                    <img class="second-section__partner" src="@/assets/images/partner_logo_3.webp" alt=".">
                    <img class="second-section__partner" src="@/assets/images/partner_logo_4.webp" alt=".">
                    <img class="second-section__partner" src="@/assets/images/partner_logo_5.webp" alt=".">
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
.second-section {
    padding-top: 50px;
    padding-bottom: 50px;
    width: 100%;
    min-height: 40vh;
    background: linear-gradient(to bottom, $second-color 12.8%, $base-color 12.8%);

    &__wrapper {
        width: 100%;
        display: flex;
        flex-direction: column;
        gap: 40px;
    }

    &__head {
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-direction: row;
    }

    &__main {
        display: flex;
        flex-direction: column;
        gap: 40px;
    }

    &__cards {
        display: grid;
        grid-template-columns: repeat(1, 1fr);
        gap: 10px;
    }

    &__divider {
        width: 100%;
        height: 1px;
        background: rgba($second-color, 0.69);
    }

    &__partners {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    &__partner {
        height: 20px;
        display: block;
    }

    &__link {
        color: $base-color;
        font-size: 0;
        font-weight: 400;
        text-decoration: none;
        display: flex;
        gap: 11px;
        align-items: center;

        &::after {
            content: '';
            background: url('@/assets/images/icon_arrow_link.svg') no-repeat center / 100%;
            width: 35px;
            height: 24px;
            display: block;
            flex-shrink: 0;
        }
    }

    @media (min-width: $mobile) {
        background: linear-gradient(to bottom, $second-color 26%, $base-color 26%);
        padding-top: 80px;
        padding-bottom: 50px;

        &__wrapper {
            gap: 50px;
        }

        &__main {
            gap: 43px;
        }

        &__cards {
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }

        &__link {
            font-size: 16px;
        }

        &__partner {
            height: 30px;
        }
    }

    @media (min-width: $tablet) {
        background: linear-gradient(to bottom, $second-color 37.8%, $base-color 37.8%);
        padding-top: 100px;
        padding-bottom: 70px;

        &__wrapper {
            gap: 60px;
        }

        &__cards {
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
        }

        &__partner {
            height: 50px;
        }
    }

    @media (min-width: $laptop) {
        padding-top: 150px;
        padding-bottom: 80px;

        &__wrapper {
            gap: 80px;
        }
    }
}
</style>
