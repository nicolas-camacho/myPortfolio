<template>
	<div class="column is-one-third">
		<article class="media notification notiVue">
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
				</div>
			</div>
		</article>
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
</style>
