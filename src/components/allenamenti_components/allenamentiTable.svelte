<script>
    import { allenamenti } from '../../stores/allenamenti/store.js';
    export let selezione = null;

    function mostraDettagli(allenamento) {
        selezione = allenamento;
    }
</script>

{#each $allenamenti as allenamento}
    <div class="scheda-allenamento">
        <h3>{allenamento.titolo}</h3>
        <p>{allenamento.descrizione}</p>
        <p class="bold">Livello: {allenamento.livello}</p>
        <p class="bold">Durata: {allenamento.durata}</p>
        <button on:click={() => mostraDettagli(allenamento)}>Vedi Dettagli</button>
    </div>
{/each}

{#if selezione}
    <div class="overlay">
        <div class="popup scheda">
            <h3>Dettagli per {selezione.titolo}</h3>
            <table>
                <thead>
                    <tr>
                        <th>Esercizio</th>
                        <th>Ripetizioni</th>
                    </tr>
                </thead>
                <tbody>
                    {#each selezione.esercizi as esercizio}
                        <tr>
                            <td>{esercizio.nome}</td>
                            <td>{esercizio.ripetizioni}</td>
                        </tr>
                    {/each}
                </tbody>
            </table>
            <button on:click={() => {selezione = null}}>Chiudi Dettagli</button>
        </div>
    </div>
{/if}

<style>
    .scheda-allenamento,
    .popup {
        padding: 1rem;
        margin-bottom: 1.5rem;
        background-color: var(--first-color);
        border-radius: 1vw;
        box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
    }

    .scheda-allenamento h3,
    .popup h3 {
        font-size: 1.25rem;
        color: var(--second-color);
        margin-bottom: 0.5rem;
    }

    .scheda-allenamento p {
        font-size: 1rem;
        color: var(--third-color);
        margin: 0.3rem 0;
    }
    .scheda-allenamento button:hover,
    .popup button:hover {
        transform: scale(1.05);
    }

    .popup table {
        width: 100%;
        border-collapse: collapse;
        margin-top: 1rem;
    }

    .popup th,
    .popup td {
        border: 1px solid var(--second-color);
        padding: 0.5rem;
        text-align: left;
        color: var(--third-color);
    }

    .popup th {
        background-color: var(--second-color);
        color: var(--first-color);
    }

    
</style>