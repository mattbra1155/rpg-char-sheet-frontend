<template>
	<div class="characters">
		<LazyCharacterList :characters="charactersData" />
		<h1>characters</h1>
	</div>
</template>

<script>
import Axios from 'axios'

export default {
	async asyncData() {
		const { data } = await Axios.get('http://localhost:3000/characters')

		console.log(data)
		return { charactersData: data }
	},
	data() {
		return {}
	},
}
</script>

<style></style>
