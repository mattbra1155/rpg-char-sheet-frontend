<template>
	<main class="main container">
		<h1 class="header">Character Sheet</h1>
		<form action="/" method="post" class="login__form">
			<div class="login__item">
				<label for="email">Email</label>
				<input type="email" name="email" />
			</div>
			<div class="login__item">
				<label for="password">Password</label>
				<input type="password" name="password" />
			</div>
			<button type="submit">Login</button>
		</form>
	</main>
</template>

<script>
import Axios from 'axios'

export default {
	data() {
		return {
			login: {
				email: '',
				password: '',
			},
		}
	},
	methods: {
		async loggin() {
			await Axios.post('####', this.login)
		},
	},
}
</script>

<style lang="scss" scoped>
.container {
	margin: 10px;
}
</style>
