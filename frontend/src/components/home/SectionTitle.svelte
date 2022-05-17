<script lang="ts">
	export let title: string;
	export let subtitle: string;
	export let centered: boolean = true;
</script>

<h2 class:text-center={centered} class="text-bold text-xs">
	<p class="uppercase text-gray-500">{subtitle}</p>
	<p class="text-4xl text-cyan-400">{title}</p>
</h2>
