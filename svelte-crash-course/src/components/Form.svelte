<script>
    import { v4 as uuidv4 } from 'uuid'; 
    import { createEventDispatcher } from 'svelte'

    let dispatch = createEventDispatcher()

    let name, price;

    const handleSubmit = () => {
        const food = {
            name: name,
            price: price,
            id: uuidv4()
        }
        dispatch("addFood", food);
    }
</script>

<form on:submit|preventDefault={handleSubmit} class="ui form">
    <div class="two fields">
        <div class="field">
            <label for="name">Food</label>
            <input bind:value={name} type="text" placeholder="Name of Food">
        </div>
        <div class="field">
            <label for="color">Price</label>
            <input bind:value={price} type="text" placeholder="Price of Food">
        </div>
        <button class="ui right labeled icon button">
            <i class="right arrow icon"></i>
                Submit
        </button>
    </div>
    
</form>