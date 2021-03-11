<script>
    import { fade } from 'svelte/transition'
    let showAlret = true;

    const hideAlret = () => {
        showAlret = false;
    };
</script>

{#if showAlret}
    <div transition:fade class="ui message">
        <i on:click={hideAlret} class="close icon"></i>
        <div class="header">
            50% off all fruits.
        </div>
        <div class="meta">Sign up for more discounts!!</div>
    </div>
{/if}
