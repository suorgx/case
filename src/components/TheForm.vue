<script>
import {defineComponent} from 'vue'
import TheInput from '@/components/TheInput.vue'
import TheMainButton from '@/components/TheMainButton.vue'
import TheTextarea from '@/components/TheTextarea.vue'

export default defineComponent({
    name: "TheForm",
    components: {
        TheInput,
        TheMainButton,
        TheTextarea
    }
})
</script>

<template>
<form class="the-form">
    <TheInput type="email" placeholder="Email" border></TheInput>
    <TheInput placeholder="Full name" border></TheInput>
    <TheTextarea placeholder="Write your massage here"></TheTextarea>
    <TheMainButton text="Submit" size="m"></TheMainButton>
</form>
</template>

<style lang="scss">
.the-form {
    width: 100%;
    display: flex;
    flex-direction: column;
    gap: 12px;

    @media (min-width: $mobile) {
        gap: 23px;
    }
}
</style>