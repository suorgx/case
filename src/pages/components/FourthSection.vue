<script>
import {defineComponent} from 'vue'
import TheCaption from '@/components/TheCaption.vue'
import TheSlider from '@/components/TheSlider.vue'

export default defineComponent({
    name: "FourthSection",
    components: {
        TheCaption,
        TheSlider
    }
})
</script>

<template>
    <section class="fourth-section">
        <div class="container fourth-section__wrapper">
            <TheCaption text="Our Blogs" base-color></TheCaption>
            <TheSlider></TheSlider>
        </div>
    </section>
</template>

<style lang="scss">
.fourth-section {
    width: 100%;
    color: $base-color;
    padding-top: 25px;
    padding-bottom: 40px;

    &__wrapper {
        display: flex;
        flex-direction: column;
        gap: 40px;
    }

    @media (min-width: $mobile) {
        padding-top: 50px;
        padding-bottom: 80px;

        &__wrapper {
            gap: 54px;
        }
    }

    @media (min-width: $tablet) {
        padding-top: 60px;
        padding-bottom: 120px;
    }

    @media (min-width: $laptop) {
        padding-top: 75px;
        padding-bottom: 150px;
    }
}
</style>
