<script>
	const img = "favicon.png";
	var name = "";
	var count = 0;

	const countHandler = () => {
		count += 1;
	}

	const inputHandler = (e) => {
		name = e.target.value;
	}
</script>

<main>
	<h1>Hi, I'm {name}!</h1>
	<input on:input={inputHandler} type="text">
	<h3>Counter: {count}</h3>
	<button on:click={countHandler}>Click</button>

	<img src={img} alt="Svelte Logo">
</main>

<style>
	main {
		display: flex;
		flex-direction: column;
		align-items: center;
	}
	h1 {
		font-size: 72px;
		text-align: center;
	}
</style>