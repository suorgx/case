<script>
import {defineComponent} from 'vue'
import TheCaption from '@/components/TheCaption.vue'
import TheCard from '@/components/TheCard.vue'

export default defineComponent({
	name: "SecondSection",
	components: {
		TheCaption,
		TheCard
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
					quotes
				</div>
				<div class="second-section__tail">
					<TheCaption text="lectus magna"></TheCaption>
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
	background: linear-gradient(to bottom, var(--second-color) 37.8%, var(--base-color) 37.8%);

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
}
</style>
