<template>
	<section class="hero is-fullheight aboutSection">
		<div class="hero-body">
			<div class="container">
			<div class="columns">
				<div class="column is-9">
					<transition appear appear-active-class="fade-enter-active">
						<article class="media notification notiVue">
							<div class="media-content">
								<div class="content">
									<h1 class="title is-size-3 has-text-white">
										<span class="colorVue">.</span>About
									</h1>
									<p class="is-size-5 has-text-white">
										Lorem ipsum dolor sit amet consectetur adipisicing elit. Minima laudantium cum voluptas voluptatibus eveniet quisquam error, asperiores harum rem eius consectetur odit quis, voluptate autem ipsum delectus obcaecati doloribus perferendis?
										Lorem ipsum dolor sit amet, consectetur adipisicing elit. Reprehenderit quisquam inventore nulla error placeat quas. Atque doloremque quam dicta necessitatibus accusantium soluta aperiam, cumque consequuntur, maxime magni, tempore reprehenderit nulla!
										Lorem ipsum, dolor sit amet consectetur adipisicing elit. Iusto commodi hic sequi officia impedit incidunt aliquid quas voluptas, repellendus harum, magni rerum molestias, nobis corporis ipsa vero reiciendis et consectetur.
									</p>
								</div>
							</div>
						</article>
					</transition>
				</div>
				<div class="column center">
					<transition appear appear-active-class="slide-enter-active">
						<img src="./../assets/imagen-perfil.jpg" class="card">
					</transition>
				</div>
			</div>
		</div>
		</div>
	</section>
</template>

<script>
export default {
	
}
</script>

<style scoped>
	.aboutSection{
		background-color: mintcream;
	}

	.card {
		width: 200px;
		border-radius: 10px;
		box-shadow: 0px 0px 0px grey;
		transition: box-shadow .6s ease-out;
		transition: width .3s ease-out;
		box-shadow: .0px .9px 3px grey;
	}

	.card:hover {
		box-shadow: 1px 8px 20px grey;
		width: 240px;
		transition: box-shadow .6s ease-in;
		transition: width .3s ease-in;
	}

	.notiVue {
		background-color: #34495E;
	}

	.colorVue {
		color: #41B883;
	}

	.center {
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.fade-enter-active{
		animation: go1 4s;
	}

	@keyframes go1{
		from{
			transform: translateX(-80px);
			opacity: 0;
		}
		to{
			transform: translateX(0px);
			opacity: 1;
		}
	}

	.slide-enter-active{
		animation: go2 4s;
	}

	@keyframes go2{
		from{
			transform: translateX(80px);
			opacity: 0;
		}
		to{
			transform: translateX(0px);
			opacity: 1;
		}
	}

</style>
