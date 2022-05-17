<script lang="ts">
	export let title: string;
	export let summary: string;
	export let image: string = 'https://via.placeholder.com/500x200?text=Work+Screenshot';
</script>

<div class="m-3" style="--bg-image:{'something'}">
	<div class="head" style={'background-image: url(' + image + ');'} />
	<h2 class="my-1">{title}</h2>
	<p class="text-gray-400 text-sm">{summary}</p>
</div>

<style lang="scss">
	.head {
		@apply w-full rounded;
		height: 200px;
		background-repeat: no-repeat;
		background-position: center;
		background-size: cover;
	}
</style>
