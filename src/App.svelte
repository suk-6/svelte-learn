<script>
	import Button from "./components/button.svelte";
	import Count from "./components/count.svelte";

	let count = 0;
	$: doubled = count * 2;

	$: if (count >= 10) {
		alert("카운트가 10이 되었습니다!");
		count = 0;
	}

	const handleClick = () => {
		count += 1;
	};
</script>

<Button {count} {handleClick} />
<Count {count} {doubled} />
