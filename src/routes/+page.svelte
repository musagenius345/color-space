<script lang="ts">
	import Slider from '../components/Nav/Slider.svelte';

	const colorSpace = [
		{
			id: 0,
			name: 'Lightness',
            value: 0.80,
			max: 100,
			min: 0,
			step: 0.5
		},
		{
			id: 1,
			name: 'Chroma',
            value: 0.10,
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

{#each colorSpace as sliderValue, id}
	<Slider colorValueName={sliderValue.name} colorValue={sliderValue.value} step={sliderValue.step} min={sliderValue.min} max={sliderValue.max}/>
{/each}


<style>
    :global(body){
    background-color: oklch(.80 0.10 225);
    }    
</style>
