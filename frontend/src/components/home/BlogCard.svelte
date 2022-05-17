<script lang="ts">
	export let title: string;
	export let image: string = 'https://via.placeholder.com/500x200?text=Featured+Image';
	export let link: string;
	export let date: string;
	export let author: string;
</script>

<div class="m-3 transition-all shadow w-4/12 rounded-lg hover:bg-teal-50 hover:shadow-lg">
	<div class="head" style={'background-image: url(' + image + ');'} />
	<a class="block px-5 pb-4" href={link}>
		<h2 class="my-1">{title}</h2>
		<p class="text-gray-400 text-sm">
			{date} <span class="inline-block w-2 h-2 ml-3 bg-gray-300 rounded-xl" /> by {author}
		</p>
	</a>
</div>

<style lang="scss">
	.head {
		@apply w-full rounded-lg rounded-b-none;
		height: 300px;
		background-repeat: no-repeat;
		background-position: center;
		background-size: cover;
	}
</style>
