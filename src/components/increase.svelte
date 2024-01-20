<script>
	import { count } from "../stores";
	const increaseHandle = () => count.update((value) => value + 1);
</script>

<button on:click={increaseHandle}>증가</button>
