<script>
	import { count } from "../stores";
	const increaseHandle = () => ($count += 1);
</script>

<button on:click={increaseHandle}>증가</button>
