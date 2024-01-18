<script>
	let todos = [
		{
			id: 1,
			content: "할일1",
			isDone: false,
		},
		{
			id: 2,
			content: "할일2",
			isDone: false,
		},
		{
			id: 3,
			content: "할일3",
			isDone: false,
		},
		{
			id: 4,
			content: "할일4",
			isDone: false,
		},
	];

	const changeState = (todo) => {
		for (let i = 0; i < todos.length; i++) {
			if (todos[i].id == todo.id) {
				todos[i].isDone = !todo.isDone;
			}
		}
	};
</script>

<ul>
	{#each todos as todo}
		<!-- svelte-ignore a11y-click-events-have-key-events -->
		{#if todo.isDone}
			<s>
				<li
					on:click={() => {
						changeState(todo);
					}}
				>
					{todo.content}
				</li>
			</s>
		{:else}
			<li
				on:click={() => {
					changeState(todo);
				}}
			>
				{todo.content}
			</li>
		{/if}
	{/each}
</ul>
