<template>
	<div class="characters">
		<div
			v-for="(character, index) in characters"
			:key="index"
			class="characters__item"
		>
			<p>{{ character.name }}</p>
			<p>{{ character._id }}</p>
		</div>
	</div>
</template>

<script>
export default {
	props: {
		characters: {
			type: Array,
			default: Array,
		},
	},
}
</script>

<style></style>
