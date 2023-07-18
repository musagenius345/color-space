<script>
	import NavBar from '../components/NavBar.svelte';
</script>

<head>
	<title>Blog</title>
	<link rel="stylesheet" href="../style.css" />
	<!-- <link rel="stylesheet" href="../normalize.css"> -->
	<meta http-equiv="X-UA-Compatible" content="ie=edge" />
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
</head>

<body>
	<NavBar />
	<div class="spacing">
		<slot>hello</slot>
	</div>
</body>

<style>
	/* Box sizing rules */
	*,
	*::before,
	*::after {
		box-sizing: border-box;
	}

	:global(:root) {
		--txt: oklch(0.07 0.16 240); /*black*/
		--accent: oklch(0.72 0.16 240); /*blue*/
		--accent-dull: oklch(0.571 0.0516 240); /*lightblue*/
		--primary: oklch(0.72 0.16 312); /*purple*/
		--primary-dark: oklch(0.42 0.21 312); /*purple*/
		--secondary: oklch(0.72 0.16 24.3); /*red*/
		--secondary-dark: oklch(0.32 0.46 24.3); /*red*/
		--surface: oklch(0.72 0.15 93.7); /*yellow*/
		--tertiary: oklch(0.72 0.15 166); /*green*/
	}

	:global(a:not(button, nav)) {
		color: var(--secondary-dark);
	}
	:global(h1,h2,h3,h4){
   color: var(--primary-dark);

	}
	@font-face {
		font-family: 'Mulish';
		src: url('/fonts/Mulish-VariableFont_wght.ttf.eot?#iefix') format('embedded-opentype'),
			url('/fonts/Mulish-VariableFont_wght.woff2') format('woff2'),
			url('/fonts/Mulish-VariableFont_wght.ttf') format('truetype');
		font-style: normal;
		font-weight: normal;
		font-display: swap;
	}

	/* Set core body defaults */
	body {
		font-family: 'Mulish', Arial, sans-serif;
		/* min-height: 100vh; */
		background-color: var(--surface);
		font-size: clamp(1rem, calc(1.25rem + 0.9vw), 1.46rem);
		text-rendering: optimizeSpeed;
		line-height: 1.5;
		accent-color: var(--accent);
	}
	.spacing {
		padding-inline: min(1.3em, 1.5rem);
	}
	@media (min-width: 500px) {
		.spacing {
			padding-inline: 4.2rem;
		}
	}
</style>
