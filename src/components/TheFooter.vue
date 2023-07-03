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
    padding-top: 50px;
    padding-bottom: 35px;
    background: $base-color;

    &__wrapper {
        display: flex;
        flex-direction: column;
        gap: 20px;
    }

    &__head {
        display: flex;
        align-items: center;
        flex-direction: column;
        gap: 20px;
    }

    &__copyright {
        color: $second-color;
        font-family: $second-font;
        font-size: 10px;
        font-weight: 700;
        opacity: 0.69;
        text-align: center;
    }

    @media (min-width: $mobile) {
        padding-top: 70px;

        &__wrapper {
            gap: 50px;
        }

        &__head {
            gap: 50px;
        }

        &__copyright {
            font-size: 12px;
        }
    }

    @media (min-width: $tablet) {
        padding-top: 80px;

        &__head {
            flex-direction: row;
            justify-content: space-between;
            gap: 10px;
        }
    }

    @media (min-width: $laptop) {
        padding-top: 100px;
        padding-bottom: 40px;

        &__wrapper {
            gap: 80px;
        }
    }
}
</style>
