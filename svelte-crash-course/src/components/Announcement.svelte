<script>
    import { fade } from 'svelte/transition'
    let showAlret = true;

    const hideAlret = () => {
        showAlret = false;
    };

    const discount = 60;
</script>

{#if showAlret}
    {#if discount < 100}
        <div transition:fade class="ui green message">
            <i on:click={hideAlret} class="close icon"></i>
            <div class="header">
                {discount}% off all fruits.
            </div>
            <div class="meta">Sign up for more discounts!!</div>
        </div>
    {/if}
    {:else}
    <div transition:fade class="ui teal message">
        <i on:click={hideAlret} class="close icon"></i>
        <div class="header">
            {discount}% off all fruits.
        </div>
        <div class="meta">Sign up for more discounts!!</div>
    </div>
{/if}
