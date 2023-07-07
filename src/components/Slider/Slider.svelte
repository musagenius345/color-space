<script lang="ts">
	export let colorValue:any
	export let colorValueName: string
	export let max: number = 100
	export let step: number = 1
	export let min: number = 0
</script>


	<div class="slider">
		
		<label for="{colorValueName}">{colorValueName}: {colorValue}</label>
		<input id='{colorValueName}' type="range" bind:value={colorValue} {max} {min} {step}/>
	</div>



<style>
	div {
		display: flex;
		flex-direction: column;
		gap: 2.5rem;
		justify-content: space-between;
		padding-inline: 1.5rem;
        background-color: transparent;
		width: 80vw;
		margin-block-end: .5rem;

		
	}

	input{
		accent-color: #15e48e;
	}
</style>
