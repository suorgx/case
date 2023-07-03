<script>
import {defineComponent} from 'vue'
import TheMainButton from '@/components/TheMainButton.vue'
import TheInput from '@/components/TheInput.vue'

export default defineComponent({
    name: "TheJoin",
    components: {
        TheMainButton,
        TheInput
    },
    props: {
        icon: Boolean
    }
})
</script>

<template>
    <form class="the-join">
        <TheInput placeholder="Enter Your Email"></TheInput>
        <TheMainButton text="Join Now" size="m"></TheMainButton>
    </form>
</template>

<style lang="scss">
.the-join {
    border-radius: 10px;
    background: $second-color;
    padding: 5px;
    color: $base-color;
    display: flex;
    align-items: center;
    gap: 5px;
    width: 100%;
    border: 1px solid rgba(125, 155, 143, 0.30);

    @media (min-width: $mobile) {
        padding: 5px 5px 5px 30px;
        gap: 10px;
    }
}
</style>