<script>
	import Timer from './Timer.svelte';
	import Timer2 from './Timer2.svelte';

	let open = false;
	let seconds = 0;

	const toggle = () => (open = !open);
	const handleTick = () => (seconds += 1);
</script>

<div>
	<button on:click={toggle}
		>{open ? 'Close' : 'Open'} Timer</button
	>
	<p>
		The Timer component has been open for
		{seconds}
		{seconds === 1 ? 'second' : 'seconds'}
	</p>
	{#if open}
		<Timer callback={handleTick} />
		<Timer2 callback={handleTick} />
	{/if}
</div>
