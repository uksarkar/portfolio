<script>
	import SectionTitle from './SectionTitle.svelte';
	import ServiceCard from './ServiceCard.svelte';

	const services = [
		{
			title: 'MERN STACK',
			subtitle: '10 Projects',
			icons: [
				{
					name: 'mongodb',
					color: '#47A248'
				},
				{
					name: 'nodedotjs',
					color: '#339933'
				},
				{
					name: 'express',
					color: '#000000'
				},
				{
					name: 'react',
					color: '#61DAFB'
				},
				{
					name: 'nginx',
					color: '#009639'
				}
			],
			summary:
				'Create project plan, Data analysis, Concept Testing, Style guide, wireframes, Concept Testing, Style guide, Responsiveness, User Testing.'
		},
		{
			title: 'MEVN STACK',
			subtitle: '5 Projects',
			icons: [
				{
					name: 'mongodb',
					color: '#47A248'
				},
				{
					name: 'nodedotjs',
					color: '#339933'
				},
				{
					name: 'express',
					color: '#000000'
				},
				{
					name: 'vuedotjs',
					color: '#4FC08D'
				},
				{
					name: 'nginx',
					color: '#009639'
				}
			],
			summary:
				'Create project plan, Data analysis, Concept Testing, Style guide, wireframes, Concept Testing, Style guide, Responsiveness, User Testing.'
		},
		{
			title: 'LAMP STACK',
			subtitle: '30 Projects',
			icons: [
				{
					name: 'linux',
					color: '#FCC624'
				},
				{
					name: 'nginx',
					color: '#009639'
				},
				{
					name: 'mysql',
					color: '#4479A1'
				},
				{
					name: 'laravel',
					color: '#FF2D20'
				}
			],
			summary:
				'Create project plan, Data analysis, Concept Testing, Style guide, wireframes, Concept Testing, Style guide, Responsiveness, User Testing.'
		}
	];
</script>

<section id="service" class="py-44 bg-gray-100">
	<SectionTitle title="Work Area" subtitle="What I will do for you" />
	<div class="container mt-20">
		<div class="service-container my-3 md:flex">
			{#each services as service}
				<div class="w-4/12"><ServiceCard {...service} /></div>
			{/each}
		</div>
	</div>
</section>

<style lang="scss">
	section {
		background: url(./images/service-bg.jpg);
		background-repeat: no-repeat;
		background-position: center;
		background-attachment: fixed;
		background-size: cover;
	}
	.service-container {
		div:not(:first-child, :last-child) {
			@apply mx-8;
		}
	}
</style>
