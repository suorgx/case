<script>
import {defineComponent} from 'vue'
import TheCaption from '@/components/TheCaption.vue'
import TheCard from '@/components/TheCard.vue'
import TheQuote from '@/components/TheQuote.vue'

export default defineComponent({
	name: "SecondSection",
	components: {
		TheCaption,
		TheCard,
		TheQuote
	}
})
</script>

<template>
	<section class="second-section">
		<div class="container">
			<div class="second-section__wrapper">
				<div class="second-section__head">
					<TheCaption text="lectus magna" base-color></TheCaption>
					Explore All
				</div>
				<div class="second-section__main">
					<div class="second-section__cards">
						<TheCard></TheCard>
						<TheCard></TheCard>
						<TheCard></TheCard>
					</div>
					<TheQuote
						name="John Doe"
						position="Founder HyperEstate"
						quote="Lorem ipsum dolor sit amet, consectetur adipiscing elit ut&nbsp;aliquam, purus sit amet luctus venenatis, lectus magna fringilla urna, porttitor."
					></TheQuote>
				</div>
				<div class="second-section__divider"></div>
				<div class="second-section__partners">
					<img class="second-section__partner" src="@/assets/images/partner_logo_1.webp" alt=".">
					<img class="second-section__partner" src="@/assets/images/partner_logo_2.webp" alt=".">
					<img class="second-section__partner" src="@/assets/images/partner_logo_3.webp" alt=".">
					<img class="second-section__partner" src="@/assets/images/partner_logo_4.webp" alt=".">
					<img class="second-section__partner" src="@/assets/images/partner_logo_5.webp" alt=".">
				</div>
			</div>
		</div>
	</section>
</template>

<style lang="scss">
.second-section {
	padding-top: 150px;
	padding-bottom: 80px;
	width: 100%;
	min-height: 40vh;
	background: linear-gradient(to bottom, $second-color 37.8%, $base-color 37.8%);

	&__wrapper {
		width: 100%;
		display: flex;
		flex-direction: column;
		gap: 80px;
	}

	&__head {
		display: flex;
		justify-content: space-between;
		align-items: center;
		flex-direction: row;
	}

	&__main {
		display: flex;
		flex-direction: column;
		gap: 43px;
	}

	&__cards {
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		gap: 30px;
	}

	&__divider {
		width: 100%;
		height: 1px;
		background: rgba($second-color, 0.69);
	}

	&__partners {
		display: flex;
		align-items: center;
		justify-content: space-between;
	}

	&__partner {
		height: 50px;
		display: block;
	}
}
</style>
