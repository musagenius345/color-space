<script>
	const NavItems = ['Home', 'Projects', 'Blog'];
</script>

<!-- <h1>Hello {name}</h1> -->

<nav>
	<ul>
		{#each NavItems as item}
			<li><a href="/{item}">{item}</a></li>
		{/each}
	</ul>
</nav>

<style>
	nav {
		max-width: 100vw;
		overflow-x: hidden;
		padding-inline: min(2ch, 1rem);
		border-block-end: 3px solid grey;
		background-color: var(--accent);
		border-radius: 1.85rem;
	}
	ul {
		display: flex;
		gap: 1rem;
		padding-block: 0.1rem;
		padding-inline: 0.5rem;
		justify-content: space-around;
		align-items: center;
		list-style: none;
	}

	a {
		text-decoration: none;
		color: navy;
		text-transform: uppercase;
		font-size: clamp(0.89rem, calc(1rem + 0.5vw), 1.4rem);
	}
</style>
