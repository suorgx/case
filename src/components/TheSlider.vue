<script>
import {defineComponent, ref} from 'vue'
import {Swiper, SwiperSlide} from 'swiper/vue'
import {Navigation} from 'swiper'
import TheSlide from '@/components/TheSlide.vue'
import 'swiper/scss'
import 'swiper/scss/navigation'

export default defineComponent({
    name: "TheSlider",
    components: {
        Swiper,
        SwiperSlide,
        TheSlide
    },
    setup() {
        const prev = ref(null);
        const next = ref(null);
        return {
            modules: [Navigation],
            prev,
            next,
        }
    }
})
</script>

<template>
    <div class="the-slider">
        <div ref="prev" class="swiper-button-prev"></div>
        <Swiper
            :navigation="{
            prevEl: prev,
            nextEl: next,
        }"
            :modules="modules"
            :slides-per-view="3"
            :space-between="30"
        >
            <SwiperSlide>
                <TheSlide
                    date="19 July 2022"
                    title="Introduction To Real Estate Investing"
                    img="slide_image_1.webp"
                ></TheSlide>
            </SwiperSlide>
            <SwiperSlide>
                <TheSlide
                    date="14 March 2022"
                    title="How I Creatively Got Into Real Estate (Twice)"
                    img="slide_image_2.webp"
                ></TheSlide>
            </SwiperSlide>
            <SwiperSlide>
                <TheSlide
                    date="28 February 2022"
                    title="The Power Of Real Estate To Create Wealth"
                    img="slide_image_3.webp"
                ></TheSlide>
            </SwiperSlide>
            <SwiperSlide>
                <TheSlide
                    date="19 July 2024"
                    title="Introduction To Real Estate Investing 2"
                    img="slide_image_1.webp"
                ></TheSlide>
            </SwiperSlide>
        </Swiper>
        <div ref="next" class="swiper-button-next"></div>
    </div>
</template>

<style lang="scss">
.the-slider {
    width: 100%;
    display: flex;

    .swiper {
        width: 90%;
    }

    .swiper-button-prev, .swiper-button-next {
        position: relative;
        left: 0;
        top: 0;
        right: 0;
        bottom: 0;
        margin: 0;
    }
}
</style>