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
    color: var(--second-color);

    &__list {
        list-style-type: none;
        display: flex;
        align-items: center;
        gap: 50px;
    }

    &__link {
        text-decoration: none;
        color: inherit;
        display: block;
        opacity: 0.8;
    }
}
</style>
