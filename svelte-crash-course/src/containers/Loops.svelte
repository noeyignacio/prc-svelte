<script>
	const fruits = [
		{name: "Apple", color: "Red", quantity: "2", id: 1},
		{name: "Orange", color: "Orange", quantity: "5", id: 2},
		{name: "Banana", color: "Yellow", quantity: "8", id: 3},
	]
</script>

<main>
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