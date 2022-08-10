<script lang="ts">
	import AddIcon from './AddIcon.svelte';
	import SubtractIcon from './SubtractIcon.svelte';

	let count = 0;
	const add = () => void (count += 1);
	const subtract = () => void (count -= 1);
</script>

<div class="counter">
	<button on:click={subtract}>
		<SubtractIcon />
	</button>
	<pre>{count}</pre>
	<button on:click={add}>
		<AddIcon />
	</button>
</div>

<style>
	.counter {
		display: grid;
		font-size: 2em;
		grid-template-columns: repeat(3, minmax(0, 1fr));
		margin-top: 2em;
		place-items: center;
	}
</style>
