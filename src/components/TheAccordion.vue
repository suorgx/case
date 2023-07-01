<script>
import {defineComponent} from 'vue'
import TheCheckbox from '@/components/TheCheckbox.vue'

export default defineComponent({
    name: "TheAccordion",
    components: {
        TheCheckbox
    },
    data() {
        return {
            items: [
                {
                    title: 'Best interest rates on the market.',
                    content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit ut aliquam, purus sit amet luctus venenatis, lectus magna fringilla',
                    isActive: true,
                },
                {
                    title: 'Prevent unstable prices',
                    content: 'accordion item 2',
                    isActive: false,
                },
                {
                    title: 'Best price on the market',
                    content: 'accordion item 3',
                    isActive: false,
                },
                {
                    title: 'Security of your data',
                    content: 'accordion item 4',
                    isActive: false,
                },
            ],
        };
    },
    methods: {
        toggleItem(index) {
            this.items.forEach((item, i) => {
                if (i === index) {
                    item.isActive = !item.isActive;
                } else {
                    item.isActive = false;
                }
            });
        },
    },
})
</script>

<template>
    <div class="the-accordion">
        <div class="the-accordion__item" v-for="(item, index) in items" :key="index">
            <div class="the-accordion__header" @click="toggleItem(index)">
                <TheCheckbox :name="item.title"></TheCheckbox>
                <span class="the-accordion__icon" :class="{ 'the-accordion__icon--active': item.isActive }">
                    <img class="third-section__left" src="@/assets/images/icon_accordion_plus.svg" alt=".">
                </span>
            </div>
            <div class="the-accordion__content" :class="{ 'the-accordion__content--active': item.isActive }">
                <div class="the-accordion__expander">
                    {{ item.content }}
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
.the-accordion {
    $parent: &;
    width: 100%;
    display: flex;
    flex-direction: column;
    gap: 22px;

    &__item {
        border-radius: 10px;
        background: $second-color;
        box-shadow: 0 0 10px 0 rgba($base-color, 0.15);
    }

    &__header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 10px;
        cursor: pointer;
    }

    &__icon {
        font-size: 20px;
        font-weight: bold;
        transition: transform 0.5s ease-in-out;

        &--active {
            transform: rotate(45deg);
        }
    }

    &__content {
        display: grid;
        grid-template-rows: 0fr;
        overflow: hidden;
        transition: grid-template-rows 0.5s;
        padding-left: 72px;
        padding-right: 16px;

        &--active {
            grid-template-rows: 1fr;
            padding-bottom: 16px;

            #{$parent}__expander {
                visibility: visible;
            }
        }
    }

    &__expander {
        min-height: 0;
        transition: visibility 1s;
        visibility: hidden;
    }
}
</style>