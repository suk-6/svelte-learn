<script lang="ts">
	import { count } from "./stores";
	import Increase from "./components/increase.svelte";
	import Decrease from "./components/decrease.svelte";
	import Result from "./components/result.svelte";

	$: if ($count < 0) {
		alert("0 이하는 금지!");
		count.set(0);
	}
</script>

<Increase />
<Decrease />
<Result />
