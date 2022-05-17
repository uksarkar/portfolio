<script lang="ts">
	const contacts = [
		{
			icon: 'H',
			body: 'House #5, Bosila, west dhanmondi. Dhaka-1120, Bandladesh'
		},
		{
			icon: 'P',
			body: '+880123456789'
		},
		{
			icon: 'E',
			body: 'utpalsarkar010@gmail.com'
		}
	];

	const toTop = () => {
		window.scrollTo({ top: 0, behavior: 'smooth' });
	};
</script>

<footer id="contact" class="bg-slate-700 px-5 py-10">
	<div class="container">
		<h2 class="text-bold text-xs text-center mb-8">
			<p class="uppercase text-gray-500">Get in touch</p>
			<p class="text-4xl text-white">Contact</p>
		</h2>
		<div class="md:flex justify-between">
			<div class="w-6/12">
				<form class="mx-10 p-6 rounded-lg bg-slate-600" action="" method="post">
					<fieldset>
						<label for="name">Your Name</label>
						<input type="text" name="name" id="name" placeholder="type name" />
					</fieldset>
					<fieldset>
						<label for="email">Your Email</label>
						<input type="email" name="email" id="email" placeholder="type email" />
					</fieldset>
					<fieldset>
						<label for="subject">Subject</label>
						<input type="text" name="subject" id="subject" placeholder="type subject" />
					</fieldset>
					<fieldset>
						<label for="message">Message</label>
						<textarea
							name="message"
							id="message"
							cols="30"
							rows="2"
							placeholder="Type your message..."
						/>
					</fieldset>
					<button class="btn btn-primary py-3 uppercase">Send Message</button>
				</form>
			</div>
			<div class="w-6/12">
				<p class="text-slate-300">
					Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis, nihil facere, eius
					unde ex omnis rerum perferendis eum natus nemo reiciendis. In harum exercitationem quas
					tenetur culpa qui ut ipsa?
				</p>
				<div class="flex items-center mt-5">
					<a class="social-icon" target="_blank" href="http://twitter.com/uksarkarr">
						<i class="utpal-icon-twitter" />
					</a>
					<a class="social-icon" target="_blank" href="http://github.com/uksarkar">
						<i class="utpal-icon-github" />
					</a>
					<a class="social-icon" target="_blank" href="http://linkedin.com/in/utpal-sarkar">
						<i class="utpal-icon-linkedin" />
					</a>
				</div>
			</div>
		</div>
		<div class="py-2 mt-3 border-t-2 border-slate-600 flex justify-between">
			<div class="text-slate-500">
				&copy; {new Date().getFullYear()} &rArr; Utpal Sarkar. All rights Reserved.
			</div>
			<div class="heart">
				<i
					on:click={toTop}
					class="cursor-pointer transition-all inline-block px-5 border rounded border-slate-500 text-slate-500 hover:text-white hover:border-white"
					title="To top"
				>
					&UpTeeArrow;
				</i>
			</div>
		</div>
	</div>
</footer>

<style lang="scss">
	form {
		fieldset {
			@apply my-3;

			label {
				@apply block uppercase text-slate-300;
			}

			textarea {
				border: 1px solid;
			}

			input,
			textarea {
				border-bottom: 1px solid;
				@apply block bg-transparent border-slate-500 focus:outline-none
					py-1 text-lg w-full placeholder:text-slate-500 text-slate-300;
			}

			textarea {
				@apply rounded px-2;
			}
		}
	}
	a.social-icon {
		@apply border-slate-500 text-slate-500 hover:bg-slate-500 hover:text-slate-400;
	}
</style>
