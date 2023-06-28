<script>
import {defineComponent} from 'vue'
import TheLogo from './TheLogo.vue'
import TheNav from './TheNav.vue'
import TheButton from './TheButton.vue'

export default defineComponent({
	name: "TheHeader",
	components: {
		TheLogo,
		TheNav,
		TheButton
	}
})
</script>

<template>
	<header class="the-header container">
		<TheLogo></TheLogo>
		<TheNav></TheNav>
		<TheButton text="Contact"></TheButton>
	</header>
</template>

<style lang="scss">
.the-header {
	padding-top: 40px;
	padding-bottom: 40px;
	background: transparent;
	display: flex;
	align-items: center;
	justify-content: space-between;
	position: absolute;
}
</style>
