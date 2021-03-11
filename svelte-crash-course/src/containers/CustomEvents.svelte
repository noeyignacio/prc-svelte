<script>
	import { v4 as uuidv4 } from 'uuid'; 
	import Form from './components/Form.svelte'

	let foods = [
		{id: uuidv4(), name: "Apple", price: 5},
		{id: uuidv4(), name: 'Orange', price: 2}
	]

	const addFood = (e) => {
		console.log(e)

		const food = e.detail
		foods = [food, ...foods]
	}
</script>

<main>
	<Form on:addFood={addFood} />
	<div class="ui cards">
		{#each foods as food (food.id)}
		<div class="card">
			<div class=content>
				<div class="header">{food.name} 
					<span class="item">
						<div class="ui red horizontal label">New</div>
					</span> 
				</div>
				<div class="meta">Price: ${food.price}</div>
				<p class="description">Tag: {food.id}</p>
			</div>
		</div>
		{/each} 
	</div>
</main>