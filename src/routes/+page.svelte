<script lang="ts">
	import Slider from '../components/Slider/Slider.svelte';
	const colorSpace = [
		{
			id: 0,
			name: 'Lightness',
			value: 0.8,
			max: 100,
			min: 0,
			step: 0.5
		},
		{
			id: 1,
			name: 'Chroma',
			value: 0.1,
			max: 1.31,
			min: 0,
			step: 0.01
		},
		{
			id: 2,
			name: 'Hue',
			value: 225,
			max: 360,
			min: 0,
			step: 0.5
		}
	];
</script>

<div class="container">
	{#each colorSpace as sliderValue, id}
		<Slider
			colorValueName={sliderValue.name}
			colorValue={sliderValue.value}
			step={sliderValue.step}
			min={sliderValue.min}
			max={sliderValue.max}

            
		/>
	{/each}
</div>

<style lang="postcss">
	@property --hue {
		syntax: '<number>';
		inherits: false;
		intial-value: 225;
	}

	@property --lightness {
		syntax: '<number>';
		inherits: false;
		intial-value: 0.8;
	}

	@property --chroma {
		syntax: '<number>';
		inherits: false;
		intial-value: 0.1;
	}

	:global(:root) {
		/* Colors */
		--lightness: 0.8;
		--chroma: 0.1;
		--hue: 225;
	}
	:global(body) {
		background-color: oklch(var(--lightness) var(--chroma) var(--hue));
		font-family: Arial, Helvetica, sans-serif;
	}

	.container {
		display: grid;
		place-items: center;
		margin-block-start: 5rem;
	}