<template>
	<div class="column is-one-third">
		<transition appear appear-active-class="fade-enter-active">
			<article class="media notification notiVue noti">
				<figure class="media-left">
					<span class="icon">
						<a :href="repo.html_url" class="has-text-white">
							<i class="fab fa-2x fa-github">	
							</i>
						</a>
					</span>
				</figure>
				<div class="media-content">
					<div class="content">
						<h1 class="title is-size-4">
							<span class="colorVue">{{repo.name}}</span>
						</h1>
						<p class="is-size-5 has-text-white">
							{{repo.description}}
						</p>
						<span class="tag is-warning">{{repo.language}}</span>
					</div>
				</div>
			</article>
		</transition>
	</div>
</template>

<script>
export default {
	props: {
		repo: Object
	}
}
</script>

<style scoped>
	.notiVue {
		background-color: #34495E;
	}

	.colorVue {
		color: #41B883;
	}

	.noti {
		border-radius: 10px;
		box-shadow: 0px 0px 0px black;
		transition: box-shadow .3s ease-out;
		box-shadow: .0px .9px 3px black;
	}

	.noti:hover {
		box-shadow: 1px 8px 20px black;
		transition: box-shadow .3s ease-in;
	}

	.fade-enter-active{
		animation: go 3s;
	}

	@keyframes go {
		from{
			transform: translateY(80px);
			opacity: 0;
		}

		to{
			opacity: 1;
		}
	}
</style>
