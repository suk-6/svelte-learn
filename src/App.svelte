<script>
	let auth = {
		loggedIn: false,
		loggedUser: null,
	};
	let userNameInput = "";

	const loginHandle = () => {
		auth.loggedIn = true;
		if (userNameInput != "") {
			auth.loggedUser = userNameInput;
		}
	};

	const logoutHandle = () => {
		auth.loggedIn = false;
	};
</script>

{#if !auth.loggedIn}
	<input type="text" bind:value={userNameInput} />
	<button on:click={loginHandle}>Login</button>
{:else}
	<input type="text" bind:value={userNameInput} disabled />
	<button on:click={logoutHandle}>Logout</button>
{/if}
