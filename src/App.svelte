<script>
	let count = 0;

	const handleClick = () => {
		count += 1;
	};
</script>

<button on:click={handleClick}>
	클릭 수: {count}
</button>
