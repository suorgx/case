<script>
import {defineComponent} from 'vue'
import TheCaption from "@/components/TheCaption.vue";

export default defineComponent({
	name: "SecondSection",
	components: {
		TheCaption
	}
})
</script>

<template>
	<section class="second-section">
		<div class="container">
			<TheCaption text="lectus magna" base-color></TheCaption>
		</div>
	</section>
</template>

<style lang="scss">
.second-section {
	padding-top: 150px;
	padding-bottom: 80px;
}
</style>
