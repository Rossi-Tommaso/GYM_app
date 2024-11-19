<script>
    import { allenamenti } from '../../stores/allenamenti/store.js';

    let nuovoAllenamento = false;
    let nuovoEsercizio = false;
    let nomeAllenamento = '';

    function creaAllenamento() {
        nuovoAllenamento = true;
    }

    function nascondiDettagli() {
        nuovoAllenamento = false;
    }

    function aggiungiAllenamento() {
        nuovoEsercizio = !nuovoEsercizio;
    }
</script>

<button class="allenamento-button" on:click={creaAllenamento}>Crea allenamento</button>

{#if nuovoAllenamento}
    <div class="overlay">
        <div class="popup">
            <div class="titolo">
                <label for="titolo">Titolo allenamento</label>
                <input type="text" name="titolo" bind:value={nomeAllenamento} placeholder="Inserisci il titolo">
            </div>

            {#if nuovoEsercizio}
                <div class="esercizio">
                    <label for="nome">Nome esercizio</label>
                    <input type="text" placeholder="Nome esercizio">
                    <label for="ripetizioni">Ripetizioni</label>
                    <input type="number" placeholder="Numero ripetizioni">
                </div>
            {/if}

            <div class="button-group">
                <button class="aggiungi-button" on:click={aggiungiAllenamento}>
                    <span>➕</span> Aggiungi esercizio
                </button>
                <button class="annulla-button" on:click={nascondiDettagli}>Annulla</button>
            </div>
        </div>
    </div>
{/if}

<style>
    :root {
        --first-color: #1e90ff;
        --second-color: #ffffff;
        --third-color: #ff6347;
        --background-overlay: rgba(0, 0, 0, 0.6);
        --border-radius: 0.8rem;
        --input-padding: 0.8rem;
        --input-margin: 0.5rem 0;
    }

    .allenamento-button {
        position: sticky;
        bottom: 0;
        margin-top: auto;
        padding: 0.8rem 1.2rem;
        font-weight: bold;
        color: var(--second-color);
        background-color: var(--first-color);
        text-align: center;
        border: none;
        border-radius: var(--border-radius);
        margin-bottom: 1rem;
        cursor: pointer;
        transition: transform 0.2s ease-in-out;
    }

    .allenamento-button:hover {
        transform: scale(1.05);
    }

    .overlay {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: var(--background-overlay);
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .titolo label, .esercizio label {
        font-weight: bold;
        margin-bottom: 0.5rem;
        display: block;
        color: #333;
    }

    .popup input {
        width: 100%;
        padding: var(--input-padding);
        margin: var(--input-margin);
        border: 1px solid #ddd;
        border-radius: var(--border-radius);
        font-size: 1rem;
    }

    .esercizio {
        margin-top: 1rem;
    }

    .button-group {
        display: flex;
        justify-content: space-between;
        margin-top: 1.5rem;
    }

    .aggiungi-button, .annulla-button {
        flex: 1;
        padding: 0.8rem 1rem;
        font-weight: bold;
        border-radius: var(--border-radius);
        cursor: pointer;
        border: none;
        transition: background 0.3s ease;
    }

    .aggiungi-button {
        background-color: var(--third-color);
        color: var(--second-color);
        margin-right: 0.5rem;
    }

    .aggiungi-button:hover {
        background-color: #ff3c26;
    }

    .annulla-button {
        background-color: #f0f0f0;
        color: #333;
        margin-left: 0.5rem;
    }

    .annulla-button:hover {
        background-color: #e0e0e0;
    }

    .aggiungi-button span {
        margin-right: 0.5rem;
    }
</style>
