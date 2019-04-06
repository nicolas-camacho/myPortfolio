<template>
	<section class="hero is-fullheight reposSection">
		<div class="hero-body">
			<div class="container">
				<div class="columns is-multiline">
					<repositories v-for="(repo, index) in reposit" :repo="repo" :key="index">
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
 .reposSection {
	background-color: #41B883;
 }
</style>
