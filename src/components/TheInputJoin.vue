<script>
import {defineComponent} from 'vue'
import TheMainButton from '@/components/TheMainButton.vue'

export default defineComponent({
    name: "TheInputJoin",
    components: {
        TheMainButton
    },
    props: {
        icon: Boolean
    }
})
</script>

<template>
    <form class="the-input-join">
        <input class="the-input-join__input" type="text" placeholder="Enter Your Email"/>
        <TheMainButton text="Join Now" size="m"></TheMainButton>
    </form>
</template>

<style lang="scss">
.the-input-join {
    border-radius: 10px;
    background: $second-color;
    padding: 5px 5px 5px 30px;
    color: $base-color;
    display: flex;
    align-items: center;
    gap: 10px;
    width: 100%;
    border: 1px solid rgba(125, 155, 143, 0.30);

    &__input {
        background: transparent;
        width: 100%;
        height: 100%;
        border: none;
        outline: none;
        font-size: 20px;
        font-weight: 400;
        letter-spacing: 0.2px;
        display: block;

        &::placeholder {
            font-size: 20px;
            font-family: $base-font;
            font-weight: 400;
            color: rgba($base-color, 0.5);
            letter-spacing: 0.2px;
        }

        &:disabled {
            opacity: 0.1;
            pointer-events: none;
        }
    }
}
</style>