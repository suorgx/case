<script>
import {defineComponent} from 'vue'

export default defineComponent({
    name: "TheModal",
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
            the modal
        </div>
    </div>
</template>

<style lang="scss">
.the-modal {
    width: 100vh;
    height: 100vh;
    position: fixed;
    background: rgba($green-color, 0.3);
    display: flex;
    align-items: center;
    justify-content: center;
    opacity: 0;
    visibility: hidden;
    transition:  opacity 0.3s, visibility 0.3s;

    &--visible {
        opacity: 1;
        visibility: visible;
    }

    &__wrapper {
        padding: 40px;
        border-radius: 10px;
        background: $second-color;
        position: relative;
    }

    &__close {
        border: none;
        background: none;
        position: absolute;
        right: 11px;
        top: 11px;
        transform: rotate(45deg);
        cursor: pointer;
    }
}
</style>