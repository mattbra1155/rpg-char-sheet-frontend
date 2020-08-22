<template>
	<main class="main container">
		<h1 class="header"></h1>
		<div class="characters">
			<div
				class="character__item"
				v-for="(character, index) in characters"
				:key="index"
			>
				<p>{{ character.name }}</p>
				<p>{{ character._id }}</p>
			</div>
		</div>
	</main>
</template>

<script>
import Axios from 'axios'
export default {
	async asyncData() {
		const { data } = await Axios.get('http://localhost:3000/characters')

		console.log(data)
		return { characters: data }
	},
	data() {
		return {
			characters: '',
		}
	},
	methods: {},
}
</script>

<style lang="scss" scoped>
.container {
	margin: 10px;
}
</style>
