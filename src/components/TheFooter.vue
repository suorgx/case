<script>
import {defineComponent} from 'vue'
import TheLogo from '@/components/TheLogo.vue'
import TheNavFooter from '@/components/TheNavFooter.vue'

export default defineComponent({
    name: "TheFooter",
    components: {
        TheLogo,
        TheNavFooter
    }
})
</script>

<template>
    <footer class="the-footer">
        <div class="container the-footer__wrapper">
            <div class="the-footer__head">
                <TheLogo></TheLogo>
                <TheNavFooter></TheNavFooter>
            </div>
            <div class="the-footer__copyright">
                Copyright &copy;&nbsp;2022 Kartik Bansal . All Rights Reseved.
            </div>
        </div>
    </footer>
</template>

<style lang="scss">
.the-footer {
    width: 100%;
    padding-top: 100px;
    padding-bottom: 40px;
    background: $base-color;

    &__wrapper {
        display: flex;
        flex-direction: column;
        gap: 80px;
    }

    &__head {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    &__copyright {
        color: $second-color;
        font-family: $second-font;
        font-size: 12px;
        font-weight: 700;
        opacity: 0.69;
        text-align: center;
    }
}
</style>
