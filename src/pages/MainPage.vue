<script>
import {defineComponent} from 'vue'

export default defineComponent({
    name: "MainPage"
})
</script>

<template>
<main class="main-page">
    <div class="container">
        main page
    </div>
</main>
</template>

<style lang="scss">
.main-page {
    width: 100%;
    background: linear-gradient(to right, var(--base-color) 75%, var(--green-color) 75%);
}
</style>
