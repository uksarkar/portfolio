<script lang="ts">
	export let icons: { name: string; color: string }[];
	export let title: string;
	export let subtitle: string;
	export let summary: string;
</script>

<div class="rounded-lg p-10 bg-white card transition-all hover:bg-cyan-50">
	<div class="icons mb-8">
		{#each icons as icon}
			<span style={`color:${icon.color}; border-color:${icon.color}`} title={icon.name}>
				<i class={`utpal-icon-${icon.name}`} />
			</span>
		{/each}
	</div>
	<h2 class="text-bold text-xs mb-1">
		<p class="uppercase text-gray-500">{subtitle}</p>
		<p class="text-4xl">{title}</p>
	</h2>
	<p class="text-gray-400 mt-4">{summary}</p>
</div>

<style lang="scss">
	$icon-mergin: 1;

	.card {
		box-shadow: 0 0 4px 2px #eee;
	}

	div.icons {
		span {
			@apply inline-flex w-12 h-12 justify-center items-center border rounded-2xl my-1 text-2xl;
			border-bottom-left-radius: 0;
			border-top-right-radius: 0;
		}
		span:not(:first-child, :last-child) {
			@apply mx-#{$icon-mergin};
		}
		span:first-child {
			@apply mr-#{$icon-mergin};
		}
		span:last-child {
			@apply ml-#{$icon-mergin};
		}
	}
</style>
