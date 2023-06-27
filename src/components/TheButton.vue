<script>
import {defineComponent} from 'vue'

export default defineComponent({
    name: "TheButton",
    props: {
        text: String
    }
})
</script>

<template>
<button class="the-button">
    {{text}}
</button>
</template>

<style scoped lang="scss">
.the-button {
    display: flex;
    padding: 20px 30px;
    align-items: flex-start;
    gap: 10px;
    border-radius: 5px;
    background: var(--second-color);
    color: var(--base-color);
    border: none;
    font-size: 20px;
    font-weight: 500;
    line-height: 100%;
    user-select: none;
}
</style>
