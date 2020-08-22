<template>
	<div>
		<Top-nav />
		<Nuxt />
	</div>
</template>

<script>
import topNav from '../components/Top-nav.vue'

export default {
	components: { 'Top-nav': topNav },
}
</script>

<style lang="scss">
* {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
}
</style>
