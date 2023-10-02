<script lang="ts">
    export let author: string = ""; 
    export let content: string = "";

</script>

<main>
    <h4>{author}</h4>
    <p>{content}</p>
</main>

<style>
    main{
        inline-size: 80%;
        padding: 3rem;
        border-radius: 12px;
        display: flex;
        flex-direction: column;
        gap: 1rem;
        background-color: #f2f2f2;
        color: #36454F;
    }
</style>