<script>
	import Button from './Button.svelte';
</script>

<section id="contact" class="contact">
	<h2 class="capitalize">Get in Touch</h2>
	<div class="contact__wrapper">
		<article class="author__detail">
			<h3 auto-capitalize>Don't be shy</h3>
			<p>
				Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ut exercitationem, dolore impedit
				incidunt sit earum nemo, sint pariatur nostrum consequatur reprehenderit labore animi culpa
				facere commodi molestiae, amet omnis officia. Vitae ipsam, nobis sequi.
			</p>
			<address class="address author__detail__info">
				<div class="author__address">
					<p class="author__heading capitalize">Address Point</p>
					<a href="Paris, Ohio" role="location">Paris, Ohio</a>
				</div>

				<div class="author__email">
					<p class="author__heading capitalize">Mail Me</p>
					<a href="mailto:johndoe@gmail.com">johndoe@gmail.com</a>
				</div>

				<div class="author__phone">
					<p class="author__heading capitalize">Call Me</p>
					<a href="tel:+12345678903">+12345678903</a>
				</div>
			</address>
		</article>

		<article class="contact__container">
			<form action="" class="contact__form">
				<fieldset>
					<legend>Fill A Form</legend>
					<input type="text" placeholder="your name" class="capitalize" />
					<input type="email" placeholder="email" class="capitalize" />
					<input type="text" placeholder="subject" class="capitalize" />

					<textarea type="text" placeholder="Your Message" class="capitalize" id="textarea" />
				</fieldset>
				<div class="terms__wrapper">
					<input type="checkbox" name="TOC" id="" class="terms__agree" required /><span
						class="terms__txt"
						>I have read and agree to the the <a href="#TOC">Terms and Conditions</a></span
					>
				</div>

				<div class="terms__wrapper">
					<input type="checkbox" name="TOC" id="" class="terms__agree" /><span class="terms__txt"
						>I agree to sign up for the Weekly newsletter</span
					>
				</div>
			</form>

			<Button>SEND MESSAGE</Button>
		</article>
	</div>
</section>

<style>
	input:not([type='checkbox']),
	textarea {
		display: block;
		width: 100%;
		background-color: transparent;
		border: 0;
		/* font-size: 1.3rem; */
		border-bottom: 2px solid var(--secondary);
		transition: all 500ms ease-in;
		outline: 0;
	}
	legend {
		color: oklch(0.32 0.16 240);
		color: oklch(from var(--acccent) calc(l - 20%) calc(c - 15%) h);
		font-weight: 800;
		line-height: 1.7;
		text-transform: uppercase;
		place-items: center;
		letter-spacing: 1ch;
		padding-inline-start: 0.8rem;
	}

	input[type='text'] {
		font: inherit;
		line-height: 2;
	}

	input[type='email'] {
		line-height: 2;
	}

	fieldset {
		display: flex;
		flex-direction: column;
		gap: 2.2rem;
		padding-inline: 1.9rem;
		padding-block: 3.2rem;

		border-style: none;
		border: 4px solid oklch(from var(--secondary) calc(l - 15%) c h);
		margin-block: 3rem;
		margin-inline: 0.43rem;
		border-radius: 0.5rem;
	}
	fieldset > :where(:not(:first-child())) {
		margin-block-start: 3.1em;
	}

	input[type='text']:is(:hover, :focus) {
		background-color: oklch(from currentColor 0.9 0.185 h);
	}

	input[placeholder]:is(:focus, :hover),
	textarea:is(:hover, :focus) {
		scale: 103.5%;
		font-size: 1.8rem;
		border-bottom-width: 4px;
	}

	::placeholder {
		font-size: 1.5rem;
		text-transform: uppercase;
		color: var(--accent-dull);
	}
</style>
