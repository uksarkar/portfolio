<script lang="ts">
	import SectionTitle from './SectionTitle.svelte';

	let working_years = new Date().getFullYear() - 2018;
</script>

<section id="about" class="container py-44">
	<div class="container">
		<div class="md:flex items-center">
			<div class="hidden md:block w-6/12">
				<img src="./images/avatar-transparent.png" alt="Avatar" srcset="" />
			</div>
			<div class="w-full md:w-6/12">
				<SectionTitle centered={false} title="About me" subtitle="Let me introduce myself" />
				<h3 class="mb-3 mt-16">A story of hadwork and persevenrance.</h3>
				<p class="text-gray-400">
					Hi, I'm Utpal Kumar Sarkar, I have a strong passion for design an development. I
					specialize in UI/UX design and development and my passion is all about building elegent
					and professional user interfaces and websites. I also do system and database design with
					MongoDB or relational database like MySQL. I've over {working_years} years of experience on
					web design and development.
				</p>
				<h3 class="my-3">Contact</h3>
				<p class="text-gray-400">
					Do you fancy saying hi to me or you want to get started with your project and you need my
					help? Feel free to contact me.
					<br />
					<b>utpalsarkar010@gmail.com</b>
				</p>
				<div class="my-3">
					<a
						class="btn btn-primary py-2 inline-block"
						href="mailto:utpalsarkar010@gmail.com?cc=utpal_sarkar@zoho.com&subject=Hello from your website&body=Hi, I want to talk to you."
						>Send Email</a
					>
					<button class="btn btn-outlined py-2">Download CV</button>
				</div>
			</div>
		</div>
	</div>
</section>
