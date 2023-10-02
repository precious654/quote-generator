<script lang="ts">
    import Icon from '@iconify/svelte';

    let word: string = '';

    function clicked() {
        console.log(word);
    }
</script>

<header>
    <div class="logo">
        <Icon icon="mdi-light:book" height='13' />
        <p>Dictionary</p>
    </div>

    <form on:submit={clicked}>
        <input type="text" placeholder="enter text..." bind:value={word}>
        <button class="search">
            <Icon icon="ic:twotone-search" height='13' />
        </button>
    </form>
</header>
<div class="vertical"></div>

<style>
    header{
        display: flex;
        justify-content: space-between;
        align-items: flex-end;
        text-transform: uppercase;
        letter-spacing: 0.2rem;
        margin-block-start: 1rem;
        font-size: 10px;
        font-weight: bold;
        font-family: 'Gowun Dodum', sans-serif;
    }

    .logo{
        display: flex; 
        gap: 0.2rem;
    }

    .vertical{
        border: 0.4px #333333 solid;
        inline-size: 100%;
        margin-block-start: 0.5rem;
    }

    form{
        position: relative;
    }

    .search{
        position: absolute;
        right: 0.25rem;
        top: 0.15rem;
    }
</style>