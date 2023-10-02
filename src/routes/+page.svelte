<script lang="ts">
    import Icon from '@iconify/svelte';

    function playAudio(){
       let audio: any = new Audio("//ssl.gstatic.com/dictionary/static/sounds/20200429/hello--_gb_1.mp3");

       audio.play();
     }

</script>

<main>
    <div>
        <div>
            <h2>Viper</h2>
            <p>/hfbfjfbf/</p>
        </div>

        <div>
            <button on:click={playAudio}>
                <Icon icon="emojione-monotone:play-button" height='36'/>
            </button>
        </div>
    </div>
    



</main>


<style>
    main{
        margin-block-start: 2rem;
    }
</style>