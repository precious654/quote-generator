<script lang="ts">
    import Card from "$lib/Card.svelte";
    import Icon from '@iconify/svelte';
    import { onMount } from "svelte";

    let quote: any = {};

    const fetchQuote = async () => {
        const response = await fetch('https://api.quotable.io/random');
        const data = await response.json();
        quote = data;
    }

    onMount( fetchQuote );

</script>

<main>
   <h1>Quote Generator</h1>
    <Card author={quote.author} content={quote.content}/>
   <div class="button">
        <button on:click={fetchQuote}>
            <Icon icon="subway:random" color="#FFF" />
        </button>
    </div>
</main>


<style>
    main{
        display: flex;
        flex-direction: column;
        gap: 0.8rem;
        align-items: center;
    }

    h1{
        margin-block-end: 0.8rem;
    }

</style>