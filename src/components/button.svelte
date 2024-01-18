<script>
	import Label from "./label.svelte";

	export let count;
	export let handleClick;
</script>

<button on:click={handleClick}>
	클릭 수: {count}
	<Label {count} />
</button>
