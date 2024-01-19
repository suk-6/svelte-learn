<script lang="ts">
	let todos = [];

	(() => {
		for (let i = 1; i < 5; i++) {
			todos.push({
				id: i,
				content: `할일 ${i}`,
				isDone: false,
			});
		}
	})();

	const changeState = (todo: object) => {
		for (let i = 0; i < todos.length; i++) {
			if (todos[i].id === todo.id) {
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
