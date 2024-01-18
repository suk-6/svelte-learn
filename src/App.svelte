<script>
	let count = 0;
	$: doubled = count * 2;

	const handleClick = () => {
		count += 1;
	};

	$: if (count >= 10) {
		alert("카운트가 10이 되었습니다!");
		count = 0;
	}

	$: {
		console.log(count);
		console.log(doubled);
	}
</script>

<button on:click={handleClick}>
	클릭 수: {count}
	{count === 1 ? "time" : "times"}
</button>

<p>두배는? {doubled}</p>
