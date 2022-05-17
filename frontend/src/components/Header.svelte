<script lang="ts">
	let links = ['Intro', 'About', 'Portfolio', 'Blog', 'Contact'];
	let isOpened: boolean = false;
	let activeLink: string = 'Intro';

	const scrollTo = (e: Event, to: string) => {
		e.preventDefault();
		document.getElementById(to)?.scrollIntoView({ behavior: 'smooth' });
	};
</script>

<div class="relative">
	<div class="container">
		<div class="flex justify-between items-center py-6 md:justify-start md:space-x-10">
			<div class="flex justify-start lg:w-0 lg:flex-1">
				<a href="/">
					<span class="sr-only">Utpal Sarkar's logo</span>
					<img
						class="h-4 w-auto sm:h-8"
						src="https://tailwindui.com/img/logos/workflow-mark-indigo-600.svg"
						alt="Utpal"
					/>
				</a>
			</div>
			<div class="-mr-2 -my-2 md:hidden">
				<button
					type="button"
					class="bg-white rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500"
					aria-expanded="false"
					on:click={() => (isOpened = true)}
				>
					<span class="sr-only">Open menu</span>
					<!-- Heroicon name: outline/menu -->
					<svg
						class="h-6 w-6"
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor"
						aria-hidden="true"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M4 6h16M4 12h16M4 18h16"
						/>
					</svg>
				</button>
			</div>
			<nav class="header-menu">
				{#each links as link}
					<a
						href="/"
						on:click={(e) => scrollTo(e, link.toLowerCase())}
						class:active={activeLink === link}
						class="link">{link}</a
					>
				{/each}
			</nav>
			<div class="hidden md:flex items-center justify-end md:flex-1 lg:w-0">
				<a class="social-icon" target="_blank" href="http://twitter.com/uksarkarr">
					<i class="utpal-icon-twitter" />
				</a>
				<a class="social-icon" target="_blank" href="http://github.com/uksarkar">
					<i class="utpal-icon-github" />
				</a>
				<a class="social-icon" target="_blank" href="http://linkedin.com/in/utpal-sarkar">
					<i class="utpal-icon-linkedin" />
				</a>
				<button
					type="button"
					on:click={(e) => {
						document.getElementById('contact')?.scrollIntoView({ behavior: 'smooth' });
					}}
					class="btn btn-outlined rounded-full ml-2"
				>
					<i class="utpal-icon-comment" />
					Chat
				</button>
			</div>
		</div>
	</div>

	<!-- Mobile only menu -->
	<div class:mobile-menu={isOpened} class:hidden={!isOpened}>
		<div
			class="rounded-lg shadow-lg ring-1 ring-black ring-opacity-5 bg-white divide-y-2 divide-gray-50"
		>
			<div class="pt-5 pb-6 px-5">
				<div class="flex items-center justify-between">
					<div>
						<img
							class="h-8 w-auto"
							src="https://tailwindui.com/img/logos/workflow-mark-indigo-600.svg"
							alt="Workflow"
						/>
					</div>
					<div class="-mr-2">
						<button
							type="button"
							class="bg-white rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500"
							on:click={() => (isOpened = false)}
						>
							<span class="sr-only">Close menu</span>
							<!-- Heroicon name: outline/x -->
							<svg
								class="h-6 w-6"
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 24 24"
								stroke="currentColor"
								aria-hidden="true"
							>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M6 18L18 6M6 6l12 12"
								/>
							</svg>
						</button>
					</div>
				</div>
				<div class="mt-6">
					<nav class="grid gap-y-8">
						<a href="/" class="link">Intro</a>
						<a href="/" class="link">About</a>
						<a href="/" class="link">Portfolio</a>
						<a href="/" class="link">Blog</a>
						<a href="/" class="link">Contact</a>
					</nav>
				</div>
			</div>
			<div class="py-6 px-5 space-y-6">
				<div class="flex items-center justify-center mx-auto">
					<a class="social-icon" href="http://twitter.com/uksarkarr">
						<img src="twitter.svg" alt="Twitter" />
					</a>
					<a class="social-icon" href="http://github.com/uksarkar">
						<img src="github.svg" alt="Github" />
					</a>
					<a class="social-icon" href="http://linkedin.com/in/utpal-sarkar">
						<img src="linkedin.svg" alt="Linked In" />
					</a>
				</div>
				<button class="btn btn-outlined w-full block text-center">Chat</button>
			</div>
		</div>
	</div>
</div>

<style lang="scss">
	nav {
		&.header-menu {
			@apply hidden md:flex space-x-10;
		}
		a {
			&.link {
				@apply relative text-base font-medium text-gray-500 hover:text-gray-900 transition-all;
				&::after {
					content: ' ';
					@apply absolute transition-all inline-block rounded-full h-1 w-0 bg-cyan-400 bottom-0 left-0;
				}
				&:hover::after {
					@apply w-full;
				}
			}

			&.active {
				@apply text-gray-900;
				&::after {
					@apply w-full;
				}
			}
		}
	}

	.mobile-menu {
		@apply absolute top-0 inset-x-0 p-2 transition-all transform origin-top-right md:hidden;
	}
</style>
