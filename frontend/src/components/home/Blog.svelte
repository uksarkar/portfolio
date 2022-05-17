<script>
	import BlogCard from './BlogCard.svelte';
	import SectionTitle from './SectionTitle.svelte';
	const blogs = [
		{
			title: 'JavaScript - zero to hero',
			date: '5 days ago',
			author: 'admin',
			image: 'https://via.placeholder.com/200x500?text=Image',
			link: 'https://blog.utpal.com/javascript-zero-to-hero'
		},
		{
			title: 'JavaScript - zero to hero',
			date: '5 days ago',
			author: 'admin',
			image: 'https://via.placeholder.com/200x500?text=Image',
			link: 'https://blog.utpal.com/javascript-zero-to-hero'
		},
		{
			title: 'JavaScript - zero to hero',
			date: '5 days ago',
			author: 'admin',
			image: 'https://via.placeholder.com/200x500?text=Image',
			link: 'https://blog.utpal.com/javascript-zero-to-hero'
		}
	];
</script>

<section id="blog" class="py-40 bg-slate-50">
	<SectionTitle title="Blog" subtitle="My Articals" />
	<div class="container mt-20">
		<div class="md:flex ">
			{#each blogs as blog}
				<BlogCard {...blog} />
			{/each}
		</div>
	</div>
</section>
