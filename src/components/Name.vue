<template>
	<section class="hero is-fullheight nameSection">
		<div class="hero-body">
			<div class="container">
				<div class="content">
					<transition appear appear-active-class="type">
						<h1 class="title has-text-white is-family-monospace">{{myName}}</h1>
					</transition>
					<transition appear appear-active-class="fade-enter-active">
						<h1 class="subtitle is-size-4 vueColor is-family-code is-italic">
							{{description}}
						</h1>
					</transition>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	data () {
		return {
			myName: "Hi I'm Nicolas Rafael Camacho Aguilar",
			description: "I'm a junior web developer with knowledge in technologies like Vue and the basics of web like HTML, CSS and offcourse javascript",
		}
	}
}
</script>

<style scoped>
	@keyframes type {
		30% { width: 0; }
	}

	@keyframes blink {
		50% { border-color: white; }
	}
	
	.nameSection {
		background-color: #34495E;
	}

	.vueColor {
		color: #41B883;
	}

	.type {
		width: 37ch;
		overflow: hidden;
		border-right: 2px solid transparent;
		font-size: 32px;
		white-space: nowrap;
		animation: type 5s steps(37), blink .8s infinite;
	}

	.fade-enter-active{
		animation: go 10s;
	}

	@keyframes go {
		from{
			opacity: 0;
		}

		to{
			opacity: 1;
		}
	}
</style>
