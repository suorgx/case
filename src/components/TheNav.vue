<script>
import {defineComponent} from 'vue'

export default defineComponent({
    name: "TheNav"
})
</script>

<template>
    <nav class="the-nav">
        <ul class="the-nav__list">
            <li class="the-nav__item">
                <a class="the-nav__link" href="#">
                    Property
                </a>
            </li>
            <li class="the-nav__item">
                <a class="the-nav__link" href="#">
                    Services
                </a>
            </li>
            <li class="the-nav__item">
                <a class="the-nav__link" href="#">
                    Product
                </a>
            </li>
            <li class="the-nav__item">
                <a class="the-nav__link" href="#">
                    About Us
                </a>
            </li>
        </ul>
    </nav>
</template>

<style lang="scss">
.the-nav {
    color: $second-color;
    font-size: 14px;

    &__list {
        list-style-type: none;
        display: flex;
        align-items: center;
        gap: 10px;
    }

    &__link {
        text-decoration: none;
        color: inherit;
        display: block;
        opacity: 0.8;
    }

    @media (min-width: $mobile) {
        font-size: 16px;

        &__list {
            gap: 40px;
        }
    }

    @media (min-width: $tablet) {
        font-size: 18px;

        &__list {
            gap: 50px;
        }
    }
}
</style>
