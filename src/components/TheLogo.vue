<script>
import {defineComponent} from 'vue'

export default defineComponent({
    name: "TheLogo"
})
</script>

<template>
    <a class="the-logo" href="#">
        HyperEstate
    </a>
</template>

<style lang="scss">
.the-logo {
    text-transform: uppercase;
    font-size: 22px;
    font-weight: 700;
    color: $second-color;
    text-decoration: none;
    display: block;
}
</style>
