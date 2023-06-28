<script>
import {defineComponent} from 'vue'

export default defineComponent({
	name: "TheButton",
	props: {
		text: String
	}
})
</script>

<template>
	<button class="the-button">
		{{ text }}
	</button>
</template>

<style lang="scss">
.the-button {
	display: flex;
	padding: 20px 30px;
	align-items: center;
	gap: 10px;
	border-radius: 5px;
	background: var(--second-color);
	color: var(--base-color);
	border: none;
	font-size: 20px;
	font-weight: 500;
	line-height: 100%;
	user-select: none;
	cursor: pointer;
	transition: background 0.5s;
	width: fit-content;

	&:hover {
		background: #E9FFF6;
	}

	&:active {
		background: #CCD7D2;
	}

	&:disabled {
		background: #D3D4D4;
		color: rgba(255, 255, 255, 0.60);
		cursor: auto;
	}
}
</style>
