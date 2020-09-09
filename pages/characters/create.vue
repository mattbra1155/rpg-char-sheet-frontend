<template>
	<div class="character-create">
		<form action="" method="post" class="character-create__form">
			<div class="from__descriptons">
				<div class="form__item">
					<label for="character-name">Name</label>
					<input
						v-model="character.name"
						type="text"
						name="character-name"
					/>
				</div>
				<div class="form__item">
					<label for="character-race">Race</label>
					<input
						v-model="character.descriptions.race"
						type="text"
						name="character-race"
					/>
				</div>
				<div class="form__item">
					<label for="character-class">Class</label>
					<input
						v-model="character.descriptions.class"
						type="text"
						name="character-class"
					/>
				</div>
				<div class="form__item">
					<label for="character-profession">Profession</label>
					<input
						v-model="character.descriptions.profession"
						type="text"
						name="character-profession"
					/>
				</div>
			</div>
			<div class="form__stats">
				<div class="form__item">
					<label for="character-speed">Speed</label>
					<input
						v-model="character.stats.speed"
						type="number"
						name="character-speed"
					/>
				</div>

				<div class="form__item">
					<label for="character-weapon-skill">Weapon Skill</label>
					<input
						v-model="character.stats['weapon skill']"
						type="number"
						name="character-weapon-skill"
					/>
				</div>

				<div class="form__item">
					<label for="character-ballistic-skill"
						>Ballistic Skill</label
					>
					<input
						v-model="character.stats['ballistic skill']"
						type="number"
						name="character-ballistic-skill"
					/>
				</div>

				<div class="form__item">
					<label for="character-strenght">Strenght</label>
					<input
						v-model="character.stats.strenght"
						type="number"
						name="character-strenght"
					/>
				</div>

				<div class="form__item">
					<label for="character-toughness">Toughness</label>
					<input
						v-model="character.stats.toughness"
						type="number"
						name="character-toughness"
					/>
				</div>
				<div class="form__item">
					<label for="character-wounds">Wounds</label>
					<input
						v-model="character.stats.wounds"
						type="number"
						name="character-wounds"
					/>
				</div>
				<div class="form__item">
					<label for="character-initiative">Initiative</label>
					<input
						v-model="character.stats.initiative"
						type="number"
						name="character-initiative"
					/>
				</div>
				<div class="form__item">
					<label for="character-attacks">Attacks</label>
					<input
						v-model="character.stats.attacks"
						type="number"
						name="character-attacks"
					/>
				</div>
				<div class="form__item">
					<label for="character-dexterity">Dexterity</label>
					<input
						v-model="character.stats.dexterity"
						type="number"
						name="character-dexterity"
					/>
				</div>
				<div class="form__item">
					<label for="character-leadership">Leadership</label>
					<input
						v-model="character.stats.leadership"
						type="number"
						name="character-leadership"
					/>
				</div>
				<div class="form__item">
					<label for="character-intelligence">Intelligence</label>
					<input
						v-model="character.stats.intelligence"
						type="number"
						name="character-intelligence"
					/>
				</div>
				<div class="form__item">
					<label for="character-cool">Cool</label>
					<input
						v-model="character.stats.cool"
						type="number"
						name="character-cool"
					/>
				</div>
				<div class="form__item">
					<label for="character-will-power">Will Power</label>
					<input
						v-model="character.stats['will power']"
						type="number"
						name="character-will-power"
					/>
				</div>
				<div class="form__item">
					<label for="character-fellowship">Fellowship</label>
					<input
						v-model="character.stats.fellowship"
						type="number"
						name="character-fellowship"
					/>
				</div>
			</div>

			<button @click="createCharacter" type="submit" class="button">
				Submit
			</button>
		</form>
	</div>
</template>

<script>
import Axios from 'axios'

export default {
	data() {
		return {
			character: {
				name: '',
				descriptions: {
					race: '',
					class: '',
					profession: '',
				},
				stats: {
					speed: '',
					'weapon skill': '',
					'ballistic skill': '',
					strenght: '',
					toughness: '',
					wounds: '',
					initiative: '',
					attacks: '',
					dexterity: '',
					leadership: '',
					intelligence: '',
					cool: '',
					'will power': '',
					fellowship: '',
				},
			},
		}
	},
	methods: {
		async createCharacter() {
			await Axios.post(
				'http://localhost:3000/characters',
				this.character
			).then((result) => {
				console.log(result)
			})
		},

		/* 		async deleteCharacter() {
			await Axios.delete('http://localhost:3000/characters')
		} */
	},
}
</script>

<style></style>
