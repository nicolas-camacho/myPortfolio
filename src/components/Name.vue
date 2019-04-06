<template>
	<section class="hero is-fullheight nameSection">
		<div class="hero-body">
			<div class="container">
				<div class="content">
					<h1 class="title is-size-2 has-text-white is-family-monospace">{{myName}}</h1>
					<h1 class="subtitle is-size-4 vueColor is-family-code is-italic">
						{{description}}
					</h1>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	data () {
		return {
			myName: 'Nicolas Rafael Camacho Aguilar',
			description: "I'm a junior web developer with knowledge in technologies like Vue and the basics of web like HTML, CSS and offcourse javascript"
		}
	}
}
</script>

<style scoped>
	.center {
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.nameSection {
		background-color: #34495E;
	}

	.vueColor {
		color: #41B883;
	}
</style>
