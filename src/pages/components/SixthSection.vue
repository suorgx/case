<script>
import {defineComponent} from 'vue'
import TheCaption from '@/components/TheCaption.vue'
import TheForm from '@/components/TheForm.vue'

export default defineComponent({
    name: "SixthSection",
    components: {
        TheCaption,
        TheForm
    }
})
</script>

<template>
    <section class="sixth-section">
        <div class="container">
            <TheCaption class="sixth-section__title" text="Contact us" base-color></TheCaption>
            <div class="sixth-section__wrapper">
                <div class="sixth-section__left">
                    <div class="sixth-section__contacts">
                        <p class="sixth-section__contact">
                            <img class="sixth-section__contact-icon" src="@/assets/images/address_icon.svg" alt=".">
                            99 something street, City, Country
                        </p>
                        <a class="sixth-section__contact" href="tel:+998999999999">
                            <img class="sixth-section__contact-icon" src="@/assets/images/phone_icon.svg" alt=".">
                            +998 (99) 999 99 99
                        </a>
                        <a class="sixth-section__contact" href="mailto:someLorem@gmail.com">
                            <img class="sixth-section__contact-icon" src="@/assets/images/email_icon.svg" alt=".">
                            someLorem@gmail.com
                        </a>
                    </div>
                    <div class="sixth-section__map">
                        <iframe title="Google Map" width="100%" height="272" frameborder="0" scrolling="no" marginheight="0"
                                marginwidth="0"
                                src="https://maps.google.com/maps?width=100%25&amp;height=272&amp;hl=en&amp;q=Tashkent+(Tashkent)&amp;t=&amp;z=14&amp;ie=UTF8&amp;iwloc=B&amp;output=embed"></iframe>
                    </div>
                </div>
                <div class="sixth-section__right">
                    <TheForm></TheForm>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
.sixth-section {
    width: 100%;
    color: $base-color;
    padding-top: 99px;
    padding-bottom: 100px;

    &__title {
        margin-bottom: 80px;
        margin-right: auto;
        margin-left: auto;
    }

    &__wrapper {
        display: flex;
        gap: 80px;
        flex-direction: row;
        align-items: flex-start;
    }

    &__left {
        max-width: 525px;
        width: 100%;
        display: flex;
        flex-direction: column;
        gap: 40px;
    }

    &__right {
        max-width: 595px;
        width: 100%;
    }

    &__contacts {
        display: flex;
        flex-direction: column;
        gap: 22px;
    }

    &__contact {
        display: flex;
        align-items: center;
        gap: 10px;
        color: $base-color;
        font-size: 20px;
        font-weight: 600;
        text-decoration: none;

        &-icon {
            width: 24px;
            height: 24px;
            flex-shrink: 0;
        }
    }

    &__map {
        border-radius: 10px;
        overflow: hidden;
    }
}
</style>
