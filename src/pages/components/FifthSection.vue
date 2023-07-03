<script>
import {defineComponent} from 'vue'
import TheCaption from '@/components/TheCaption.vue'
import TheJoin from '@/components/TheJoin.vue'

export default defineComponent({
    name: "FifthSection",
    components: {
        TheJoin,
        TheCaption
    }
})
</script>

<template>
    <section class="fifth-section">
        <div class="container fifth-section__wrapper">
            <TheCaption tag="h3" text="Ready to get started?" font="third"></TheCaption>
            <p class="fifth-section__description">
                To join the worldwide community
            </p>
            <div class="fifth-section__input">
                <TheJoin></TheJoin>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
.fifth-section {
    background: $base-color;
    padding-bottom: 50px;
    padding-top: 50px;

    &__wrapper {
        display: flex;
        align-items: center;
        flex-direction: column;
        gap: 18px;
    }

    &__description {
        color: rgba($second-color, 0.8);
        font-size: 17px;
        font-family: $third-font;
        font-style: normal;
        font-weight: 600;
        line-height: 144%;
        letter-spacing: 0.46px;
    }

    &__input {
        max-width: 612px;
        width: 100%;
        margin-top: 40px;
    }

    @media (min-width: $mobile) {
        padding-bottom: 60px;
        padding-top: 60px;

        &__description {
            font-size: 19px;
        }
    }

    @media (min-width: $tablet) {
        padding-bottom: 100px;
        padding-top: 100px;

        &__description {
            font-size: 21px;
        }

        &__input {
            margin-top: 50px;
        }
    }

    @media (min-width: $laptop) {
        padding-bottom: 150px;
        padding-top: 145px;

        &__description {
            font-size: 23px;
        }

        &__input {
            margin-top: 63px;
        }
    }
}
</style>