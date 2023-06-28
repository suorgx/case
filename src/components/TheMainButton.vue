<script>
import {defineComponent} from 'vue'

export default defineComponent({
	name: "TheMainButton",
	props: {
		text: String
	}
})
</script>

<template>
	<button class="the-main-button">
		{{ text }}
	</button>
</template>

<style lang="scss">
.the-main-button {
	display: flex;
	padding: 25px 30px;
	align-items: center;
	gap: 10px;
	border-radius: 10px;
	background: var(--green-color);
	color: var(--second-color);
	border: none;
	font-size: 20px;
	font-weight: 700;
	letter-spacing: 0.2px;
	line-height: 100%;
	user-select: none;
	cursor: pointer;
	transition: background 0.5s;
	width: fit-content;

	&:hover {
		background: #94B9A9;
	}

	&:active {
		background: #6B7D76;
	}

	&:disabled {
		background: #D3DCD8;
		color: #F5F5F5;
		cursor: auto;
	}
}
</style>
