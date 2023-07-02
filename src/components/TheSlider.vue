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
                    img="1"
                ></TheSlide>
            </SwiperSlide>
            <SwiperSlide>
                <TheSlide
                    date="14 March 2022"
                    title="How I Creatively Got Into Real Estate (Twice)"
                    img="2"
                ></TheSlide>
            </SwiperSlide>
            <SwiperSlide>
                <TheSlide
                    date="28 February 2022"
                    title="The Power Of Real Estate To Create Wealth"
                    img="3"
                ></TheSlide>
            </SwiperSlide>
            <SwiperSlide>
                <TheSlide
                    date="19 July 2024"
                    title="Introduction To Real Estate Investing 2"
                    img="4"
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
        width: 91%;
    }

    .swiper-button-prev, .swiper-button-next {
        position: relative;
        left: 0;
        top: 0;
        right: 0;
        bottom: 0;
        margin: 0;
        border-radius: 5px;
        background: rgba($green-color, 0.30);
        width: 32px;
        height: 32px;
        overflow: hidden;

        &:after {
            content: '';
            background: url('@/assets/images/icon_arrow_slider.svg') no-repeat center / 100%;
            width: 16px;
            height: 16px;
            display: block;
            flex-shrink: 0;
        }
    }

    .swiper-button-next:after {
        transform: rotate(180deg);
    }
}
</style>