<script>
import {defineComponent} from 'vue'
import TheCaption from '@/components/TheCaption.vue'

export default defineComponent({
	name: "FirstSection",
	components: {
		TheCaption
	}
})
</script>

<template>
	<section class="first-section">
		<div class="container first-section__wrapper">
			<div class="first-section__left">
				<TheCaption text="Lectus Magna Fringilla Urna, Porttitor"></TheCaption>
				<p class="first-section__description">
					Lorem ipsum dolor sit amet, consectetur adipiscing elit ut&nbsp;aliquam, purus sit amet luctus
					venenatis, lectus magna fringilla urna, porttitor.
				</p>
			</div>
			<img class="first-section__right" src="@/assets/images/content_image_1.png" alt="">
		</div>
	</section>
</template>

<style scoped lang="scss">
.first-section {
	background: linear-gradient(to right, var(--base-color) 61.2%, var(--green-color) 61.2%);
	width: 100%;
	color: var(--second-color);
	padding-top: 200px;
	padding-bottom: 100px;

	&__wrapper {
		display: flex;
		gap: 98px;
		flex-direction: row;
		align-items: flex-start;
	}

	&__left {
		display: flex;
		flex-direction: column;
		gap: 28px;
		position: relative;
	}

	&__right {
		max-width: 603px;
		width: 100%;
		display: block;
	}

	&__description {
		color: #FFF;
		font-size: 18px;
		font-weight: 500;
		line-height: 110%;
		text-transform: capitalize;
		opacity: 0.8;
	}

}
</style>
