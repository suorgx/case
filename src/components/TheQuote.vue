<script>
import {defineComponent} from 'vue'

export default defineComponent({
    name: "TheQuote",
    props: {
        name: String,
        position: String,
        quote: String
    }
})
</script>

<template>
    <div class="the-quote">
        <div class="the-quote__info">
            <div class="the-quote__name">
                {{ name }}
            </div>
            <div class="the-quote__position">
                {{ position }}
            </div>
        </div>
        <div class="the-quote__quote">
            {{ quote }}
        </div>
    </div>
</template>

<style lang="scss">
.the-quote {
    width: 100%;
    color: $second-color;
    display: flex;
    align-items: flex-start;
    flex-direction: column;
    justify-content: space-between;
    gap: 10px;

    &__info {
        display: flex;
        flex-direction: column;
        gap: 10px;
    }

    &__name {
        font-size: 22px;
        font-weight: 700;
    }

    &__position {
        font-size: 15px;
        font-weight: 500;
        opacity: 0.8;
    }

    &__quote {
        font-size: 22px;
        color: rgba($second-color, 0.8);
        font-weight: 700;
        line-height: 150%;
        max-width: 665px;
        display: flex;
        align-items: flex-start;
        flex-direction: column;
        gap: 6px;

        &::before {
            content: '';
            background: url('@/assets/images/icon_quote.svg') no-repeat center / 100%;
            width: 40px;
            height: 40px;
            display: block;
            flex-shrink: 0;
            margin-top: -5px;
        }
    }

    @media (min-width: $mobile) {
        flex-direction: row;

        &__name {
            font-size: 28px;
        }

        &__position {
            font-size: 18px;
        }

        &__quote {
            font-size: 28px;
            flex-direction: row;
            gap: 16px;
        }
    }
}
</style>
