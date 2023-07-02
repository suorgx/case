<script>
import {defineComponent} from 'vue'
import TheForm from '@/components/TheForm.vue'
import TheCaption from "@/components/TheCaption.vue";

export default defineComponent({
    name: "TheModal",
    components: {
        TheForm
    },
    props: {
        isVisible: Boolean
    }
})
</script>

<template>
    <div class="the-modal"
         :class="{ 'the-modal--visible': isVisible }"
         @click.self="$emit('closeModal')"
         ref="modal"
    >
        <div class="the-modal__wrapper">
            <button class="the-modal__close" @click="$emit('closeModal')">
                <img class="the-modal__img" src="@/assets/images/icon_accordion_plus.svg" alt=".">
            </button>
            <TheForm></TheForm>
        </div>
    </div>
</template>

<style lang="scss">
.the-modal {
    width: 100%;
    padding-right: 5px;
    padding-left: 5px;
    height: 100vh;
    position: fixed;
    background: rgba($green-color, 0.3);
    display: flex;
    align-items: center;
    justify-content: center;
    opacity: 0;
    visibility: hidden;
    transition:  opacity 0.3s, visibility 0.3s;
    z-index: 1;

    &--visible {
        opacity: 1;
        visibility: visible;
    }

    &__wrapper {
        padding: 10px;
        border-radius: 10px;
        background: $second-color;
        position: relative;
        max-width: 675px;
        width: 100%;
    }

    &__close {
        border: none;
        background: none;
        transform: rotate(45deg);
        cursor: pointer;
        margin-left: auto;
        margin-bottom: 10px;
        display: block;
    }

    &__img {
        display: block;
    }

    @media (min-width: $mobile) {
        padding-right: 10px;
        padding-left: 10px;

        &__wrapper {
            padding: 40px;
        }

        &__close {
            position: absolute;
            right: 11px;
            top: 11px;
            margin-left: 0;
            margin-bottom: 0;
        }
    }
}
</style>