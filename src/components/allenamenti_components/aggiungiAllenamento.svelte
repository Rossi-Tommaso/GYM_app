<script>
    import { allenamenti } from '../../stores/allenamenti/store.js';

    let nuovoAllenamento = false;
    let nomeAllenamento = '';

    function creaAllenamento() {
        nuovoAllenamento = true;
    }

    function nascondiDettagli() {
        nuovoAllenamento = false;
    }
</script>

<button class="allenamento-button" on:click={creaAllenamento}>Crea allenamento</button>

{#if nuovoAllenamento}
    <div class="overlay">
        <div class="popup scheda">
            <label for="titolo">Titolo allenamento</label>
            <input type="text" name="titolo" bind:value={nomeAllenamento}>
            <button on:click={nascondiDettagli}>Annulla</button>
        </div>
    </div>
{/if}

<style>
    .allenamento-button {
        position: sticky;
        bottom: 0;
        margin-top: auto;
        padding: 0.8rem;
        font-weight: bold;
        color: var(--first-color);
        text-align: center;
        border-radius: 0.5vw;
        margin-bottom: 1rem;
    }
</style>