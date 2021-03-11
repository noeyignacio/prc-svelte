<script>
	let name;
	let num;
	let isChecked = false;
	let value = 1;
	let selected;

	let questions = [
		{id: 1, text: 'What is 1?'},
		{id: 2, text: 'What is 2?'}
	]
</script>

<main>
	<input type="text" bind:value={name}>
	<input type="number" bind:value={num}>
	<input type="checkbox" bind:value={isChecked}>

	<label>
		<input type="radio" bind:group={value} value={1}>1
	</label>
	<label>
		<input type="radio" bind:group={value} value={2}>2
	</label>
	<label>
		<input type="radio" bind:group={value} value={3}>3
	</label>

	<select bind:value={selected}>
		{#each questions as question}
			<option value={question}>{question.text}</option>
		{/each}
	</select>
</main>