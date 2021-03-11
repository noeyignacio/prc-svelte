<script>
	var firstName = "";
	var lastName = "";

	/* Reactive Values */
	$: fullName = `${firstName} ${lastName}`
	const resetFullName = () => {
		fullName = ""
		document.querySelector(".firstName").value = "";
		document.querySelector(".lastName").value = "";
	}
</script>

<main>
    <h1>Hello, I'm {fullName}!</h1>
	
	<label for="firstName">First Name:</label>
	<input bind:value={firstName} class="firstName" type="text">
	<label for="lastName">Last Name:</label>
	<input bind:value={lastName} class="lastName" type="text">
	<button on:click={resetFullName}>Reset Full Name</button>

</main>