<script>
	import PortfolioCard from './PortfolioCard.svelte';
	import SectionTitle from './SectionTitle.svelte';

	const works = [
		{
			title: 'Gpoint - Factory management system',
			summary: "It's a germent's factory management system.",
			image: 'https://via.placeholder.com/500x200?text=Gpoint'
		},
		{
			title: 'Gpoint - Factory management system',
			summary: "It's a germent's factory management system.",
			image: 'https://via.placeholder.com/500x200?text=Gpoint'
		},
		{
			title: 'Gpoint - Factory management system',
			summary: "It's a germent's factory management system.",
			image: 'https://via.placeholder.com/500x200?text=Gpoint'
		},
		{
			title: 'Gpoint - Factory management system',
			summary: "It's a germent's factory management system.",
			image: 'https://via.placeholder.com/500x200?text=Gpoint'
		}
	];
</script>

<section id="portfolio" class="py-40">
	<SectionTitle title="Portfolio" subtitle="Some of my recent work" />
	<div class="container mt-20">
		<div class="md:flex">
			{#each works as work}
				<PortfolioCard {...work} />
			{/each}
		</div>
	</div>
</section>
