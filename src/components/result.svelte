<script>
	import { count } from "../stores";

	let visibleValue;

	(() => {
		count.subscribe((value) => {
			visibleValue = value;
		});
	})();
</script>

<p>{visibleValue}</p>
