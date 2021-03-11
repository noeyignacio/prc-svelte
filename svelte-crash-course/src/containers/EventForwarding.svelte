<script>
	import Button from './components/Button.svelte'

	const log = () => {
		console.log("Button Clicked!")
	}
</script>

<main>
	<Button on:click={log} buttonText={"Hello Earth!"}/>
	<button on:click={log} class="ui green button">Hello Mars!</button>
</main>