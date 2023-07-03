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
                        <iframe title="Tashkent Google Map" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d95942.66986227602!2d69.1967956811091!3d41.28256795107951!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38ae8b0cc379e9c3%3A0xa5a9323b4aa5cb98!2sTashkent%2C%20Uzbekistan!5e0!3m2!1sen!2sus!4v1688302533441!5m2!1sen!2sus" width="100%" height="272" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
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
    padding-top: 50px;
    padding-bottom: 50px;

    &__title {
        margin-bottom: 40px;
        margin-right: auto;
        margin-left: auto;
    }

    &__wrapper {
        display: flex;
        gap: 40px;
        flex-direction: column;
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
        gap: 16px;
    }

    &__contact {
        display: flex;
        align-items: center;
        gap: 10px;
        color: $base-color;
        font-size: 16px;
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

    @media (min-width: $mobile) {
        padding-top: 60px;
        padding-bottom: 60px;

        &__title {
            margin-bottom: 50px;
        }

        &__wrapper {
            gap: 50px;
        }

        &__contact {
            font-size: 20px;
        }

        &__contacts {
            gap: 22px;
        }
    }

    @media (min-width: $tablet) {
        padding-top: 80px;
        padding-bottom: 80px;

        &__title {
            margin-bottom: 65px;
        }

        &__wrapper {
            flex-direction: row;
        }
    }

    @media (min-width: $laptop) {
        padding-top: 100px;
        padding-bottom: 100px;

        &__title {
            margin-bottom: 80px;
        }

        &__wrapper {
            gap: 80px;
        }
    }
}
</style>
