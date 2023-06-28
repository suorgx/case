<script>
import {defineComponent} from 'vue'

export default defineComponent({
	name: "TheChip"
})
</script>

<template>
<div class="the-chip">
	<img class="the-chip__icon" src="@/assets/images/card_icon_link.svg" alt="" />
	<div class="the-chip__name">
		2500 sqft
	</div>
</div>
</template>

<style lang="scss">
.the-chip {
	border-radius: 5.5px;
	background: var(--second-color);
	box-shadow: 0 0 6.5px 0 rgba(20, 20, 20, 0.15);
	display: flex;
	padding: 10px;
	justify-content: center;
	align-items: center;
	gap: 10px;
	width: 100%;

	&__icon {
		width: 12px;
		height: 12px;
		display: block;
	}

	&__name {
		color: var(--base-color);
		font-size: 16px;
		font-weight: 700;
		line-height: 100%;
	}
}
</style>
