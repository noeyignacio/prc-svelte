<script>
	let fruits = [
		{name: "Apple", color: "Red", quantity: "2", id: 1},
		{name: "Orange", color: "Orange", quantity: "5", id: 2},
		{name: "Banana", color: "Yellow", quantity: "8", id: 3},
	]

	const deleteFruit = (id) => {

		/* If True: `fruit` will be kept. */
		/* False: `fruit` will be remove. */
		fruits = fruits.filter((fruit) => fruit.id != id) 
		console.log(fruits)
	}
</script>

<main>
	{#each fruits as fruit (fruit.id)}
		{#if fruit.quantity > 4}
			<div class="ui cards">
				<div class="card">
					<div class="content">
						<div class="header">{fruit.name}</div>
						<div class="meta">Quantity: {fruit.quantity}</div>
						<div class="description">Color: {fruit.color}</div>
					</div>
					<button class="ui red button" on:click={() => deleteFruit(fruit.id)}>Delete</button>
				</div>
			</div>
		{/if}
	{:else}
		<p>There is no Fruits.</p>
	{/each}
</main>