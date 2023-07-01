<script>
import {defineComponent} from 'vue'

export default defineComponent({
    name: "TheNavFooter"
})
</script>

<template>
    <nav class="the-nav-footer">
        <ul class="the-nav-footer__list">
            <li class="the-nav-footer__item the-nav-footer__item--active">
                <a class="the-nav-footer__link" href="#">
                    Home
                </a>
            </li>
            <li class="the-nav-footer__item">
                <a class="the-nav-footer__link" href="#">
                    About
                </a>
            </li>
            <li class="the-nav-footer__item">
                <a class="the-nav-footer__link" href="#">
                    Service
                </a>
            </li>
            <li class="the-nav-footer__item">
                <a class="the-nav-footer__link" href="#">
                    Portfolio
                </a>
            </li>
            <li class="the-nav-footer__item">
                <a class="the-nav-footer__link" href="#">
                    Blog
                </a>
            </li>
            <li class="the-nav-footer__item">
                <a class="the-nav-footer__link" href="#">
                    Contact
                </a>
            </li>
        </ul>
    </nav>
</template>

<style lang="scss">
.the-nav-footer {
    $parent: &;

    &__list {
        list-style-type: none;
        display: flex;
        align-items: center;
        gap: 40px;
    }

    &__item {
        color: rgba($green-color, 0.90);
        font-size: 16px;
        font-weight: 700;

        &--active {
            color: $second-color;
        }
    }

    &__link {
        text-decoration: none;
        color: inherit;
        display: block;
    }
}
</style>
