<script>
	// const img = "favicon.png";
	// var name = "Francis";
	// var count = 0;

	// /* Count Handlers */
	// const countHandler = () => {
	// 	count += 1;
	// }
	// const resetCountHandler = () => {
	// 	count = 0;
	// }

	// /* Input Handlers */
	// const inputHandler = (e) => {
	// 	name = e.target.value;
	// }
	// const deleteInputHandler = () => {
	// 	name = "";
	// 	document.querySelector(".inputHandler").value = ""
	// }

	// var firstName = "";
	// var lastName = "";

	// /* Reactive Values */
	// $: fullName = `${firstName} ${lastName}`
	// const resetFullName = () => {
	// 	fullName = ""
	// 	document.querySelector(".firstName").value = "";
	// 	document.querySelector(".lastName").value = "";
	// }

	const fruits = [
		{name: "Apple", color: "Red", quantity: "2", id: 1},
		{name: "Orange", color: "Orange", quantity: "5", id: 2},
		{name: "Banana", color: "Yellow", quantity: "8", id: 3},
	]
</script>

<main>
	<!-- <h1>Hi, I'm {name}!</h1>
	<input on:input={inputHandler} class="inputHandler" type="text">
	<button on:click={deleteInputHandler}>Reset Name</button>

	<h3>Counter: {count}</h3>
	<button on:click={countHandler}>Click</button>
	<button on:click={resetCountHandler}>Reset Count</button> -->

	<!-- <h1>Hello, I'm {fullName}!</h1>
	
	<label for="firstName">First Name:</label>
	<input bind:value={firstName} class="firstName" type="text">
	<label for="lastName">Last Name:</label>
	<input bind:value={lastName} class="lastName" type="text">
	<button on:click={resetFullName}>Reset Full Name</button>

	<img src={img} alt="Svelte Logo"> -->

	{#each fruits as fruit (fruit.id)}
		<div class="ui cards">
			<div class="card">
				<div class="content">
					<div class="header">{fruit.name}</div>
					<div class="meta">Quantity: {fruit.quantity}</div>
					<div class="description">Color: {fruit.color}</div>
				</div>
			</div>
		</div>
	{:else}
		<p>There is no Fruits.</p>
	{/each}
</main>