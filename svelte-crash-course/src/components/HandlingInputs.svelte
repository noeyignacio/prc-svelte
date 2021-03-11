<script>
	const img = "favicon.png";
	var name = "Francis";
	var count = 0;

	/* Count Handlers */
	const countHandler = () => {
		count += 1;
	}
	const resetCountHandler = () => {
		count = 0;
	}

	/* Input Handlers */
	const inputHandler = (e) => {
		name = e.target.value;
	}
	const deleteInputHandler = () => {
		name = "";
		document.querySelector(".inputHandler").value = ""
	}
</script>

<main>
	<h1>Hi, I'm {name}!</h1>
	<input on:input={inputHandler} class="inputHandler" type="text">
	<button on:click={deleteInputHandler}>Reset Name</button>

	<h3>Counter: {count}</h3>
	<button on:click={countHandler}>Click</button>
	<button on:click={resetCountHandler}>Reset Count</button>

	<img src={img} alt="Svelte Logo"> -->

</main>