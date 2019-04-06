<template>
	<section class="hero is-fullheight">
		<div class="hero-body">
			<div class="container">
				<div class="columns is-multiline">
					<repositories v-for="repo in reposit" :repo="repo">
					</repositories>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
import repositories from './Repositorie.vue'
export default {
	components: {
		repositories
	},
	data (){
		return{
			reposit: []
		}
	},
	async mounted() {
		const response = await fetch("https://api.github.com/users/nicolas-camacho/repos")
		this.reposit = await response.json()
	}
}
</script>

<style scoped>

</style>
