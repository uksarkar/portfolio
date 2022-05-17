<script>
	import Header from '../Header.svelte';
</script>

<div id="intro" class="hero">
	<Header />

	<div class="container">
		<div class="md:flex items-center" style="height: calc(100vh - 82px);">
			<div class="w-6/12">
				<h1 class="font-bold uppercase text-base">
					Hello, I'm a
					<br />
					<b class="text-4xl"
						>Full stack
						<span class="text-teal-400 underline underline-offset-2"> web developer. </span>
					</b>
				</h1>
				<p class="text-gray-700 my-5 w-80">
					Hi, I'm Utpal Kumar Sarkar, a passionate Full-stack web developer. Welcome to my portfolio
					area.
				</p>
				<div class="text-center md:text-left">
					<button
						type="button"
						on:click={(e) => {
							document.getElementById('portfolio')?.scrollIntoView({ behavior: 'smooth' });
						}}
						class="btn btn-primary uppercase py-3"
					>
						View Portfolio
					</button>
				</div>
			</div>
			<div class="w-6/12">
				<img src="./images/test3.png" alt="Avatar" srcset="" />
			</div>
		</div>
	</div>
</div>

<style lang="scss">
	.hero {
		max-height: 100vh;
		background-attachment: fixed;
		background-image: url(/gray-abstract-textured-background.jpg);
		background-repeat: no-repeat;
		background-position: center;
		background-size: cover;
	}
</style>
