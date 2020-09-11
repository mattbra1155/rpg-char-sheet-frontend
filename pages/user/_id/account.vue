<template>
	<div>
		<h1>Account {{ userId }}</h1>
	</div>
</template>

<script>
export default {
	data() {
		return {
			userId: this.getPageParams().id,
		}
	},
	methods: {
		getPageParams() {
			console.log(this.$route.params)
			return this.$route.params
		},
	},
}
</script>

<style></style>
