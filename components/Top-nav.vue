<template>
	<nav class="nav">
		<div class="nav__item">
			<nuxt-link to="/">Home</nuxt-link>
		</div>
		<div class="nav__item">
			<nuxt-link to="/characters/">Characters</nuxt-link>
		</div>
		<div class="nav__item">
			<a href="#">Link</a>
		</div>
		<div class="nav__item">
			<a href="#">Link</a>
		</div>
	</nav>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
@import '~/assets/styles/scss/_mixins.scss';
.nav {
	@include flex(row, space-evenly, center);
	height: 10vh;
	background: #bbb;
}
</style>
