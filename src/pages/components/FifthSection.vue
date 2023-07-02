<script>
import {defineComponent} from 'vue'
import TheCaption from '@/components/TheCaption.vue'
import TheInputJoin from '@/components/TheInputJoin.vue'

export default defineComponent({
    name: "FifthSection",
    components: {
        TheInputJoin,
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
                <TheInputJoin></TheInputJoin>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
.fifth-section {
    background: $base-color;
    padding-bottom: 150px;
    padding-top: 145px;

    &__wrapper {
        display: flex;
        align-items: center;
        flex-direction: column;
        gap: 18px;
    }

    &__description {
        color: rgba($second-color, 0.8);
        font-size: 23px;
        font-family: $third-font;
        font-style: normal;
        font-weight: 600;
        line-height: 144%;
        letter-spacing: 0.46px;
    }

    &__input {
        max-width: 612px;
        width: 100%;
        margin-top: 63px;
    }
}
</style>