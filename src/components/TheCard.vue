<script>
import {defineComponent} from 'vue'

export default defineComponent({
	name: "TheCard"
})
</script>

<template>
	<div class="the-card">
		<img class="the-card__image" src="@/assets/images/content_image.webp" alt=".">
		<div class="the-card__info">
			<div class="the-card__price">
				$ 59,345
			</div>
			<div class="the-card__name">
				Lorem ipsum dolor sit
			</div>
			<div class="the-card__divider"></div>
			<div class="the-card__chips">
				2 1 1
			</div>
		</div>
	</div>
</template>

<style lang="scss">
.the-card {
	width: 100%;
	border-radius: 10px;
	overflow: hidden;
	background: var(--second-color);

	&__image {
		width: 100%;
		height: 280px;
		display: block;
		object-fit: cover;
	}

	&__info {
		padding: 32px;
		display: flex;
		flex-direction: column;
		gap: 22px;
	}

	&__divider {
		width: 100%;
		height: 1px;
		flex-shrink: 0;
		background: var(--base-color);
	}

	&__price {
		color: var(--base-color);
		font-size: 24px;
		font-weight: 700;
		line-height: 100%;
	}

	&__name {
		color: var(--base-color);
		font-size: 20px;
		font-weight: 700;
	}
}
</style>
