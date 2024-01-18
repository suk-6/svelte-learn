<script>
	export let count;
	export let doubled;

	$: {
		console.log(count);
		console.log(doubled);
	}
</script>
