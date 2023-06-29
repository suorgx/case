<script>
import {defineComponent} from 'vue'

export default defineComponent({
	name: "TheCaption",
	props: {
		text: String,
		baseColor: {
			type: Boolean,
			default: false
		},
		tag: {
			type: String,
			default: "h2"
		}
	}
})
</script>
<template>
	<component
		:is="tag"
		class="the-caption"
		:class="baseColor ? 'the-caption--base-color' : 'the-caption--second-color'"
	>
		{{ text }}
	</component>
</template>

<style lang="scss">
.the-caption {
	color: $second-color;
	font-size: 58px;
	font-weight: 700;

	&--base-color {
		color: $base-color;
	}

	&--second-color {
		color: $second-color;
	}
}
</style>
