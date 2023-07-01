<script>
import {defineComponent} from 'vue'

export default defineComponent({
    name: "TheCheckbox",
    props: {
        name: String
    }
})
</script>

<template>
    <label class="the-checkbox">
        <input class="the-checkbox__input" type="checkbox" checked="checked">
        <span class="the-checkbox__checkmark"></span>
        <span class="the-checkbox__name">
            {{ name }}
        </span>
    </label>
</template>

<style lang="scss">
.the-checkbox {
    $parent: &;

    display: flex;
    align-items: center;
    gap: 24px;
    cursor: pointer;
    font-size: 22px;
    user-select: none;

    &__input {
        position: absolute;
        opacity: 0;
        cursor: pointer;
        height: 0;
        width: 0;
    }

    &__checkmark {
        height: 32px;
        width: 32px;
        background-color: rgba($green-color, 0.3);
        border-radius: 5px;
        display: flex;
        align-items: center;
        justify-content: center;

        &:after {
            content: "";
            display: none;
            width: 6px;
            height: 12px;
            margin-top: -4px;
            border: solid $green-color;
            border-width: 0 3px 3px 0;
            transform: rotate(45deg);
        }
    }

    #{$parent}__input:checked ~ #{$parent}__checkmark:after {
        display: block;
    }

    &__name {
        color: $base-color;
        font-size: 18px;
        font-style: normal;
        font-weight: 700;
        line-height: 150%;
        text-transform: capitalize;
    }
}
</style>