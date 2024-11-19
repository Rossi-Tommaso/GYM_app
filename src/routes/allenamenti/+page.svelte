<script>
    import AllenamentiTable from "../../components/allenamenti_components/allenamentiTable.svelte";
    import AggiungiAllenamento from "../../components/allenamenti_components/aggiungiAllenamento.svelte";
</script>

<div class="container">
    <div class="section">
        <h2 class="faculty-glyphic-regular bold">I tuoi allenamenti:</h2>

        <AllenamentiTable />

        <AggiungiAllenamento />
    </div>
</div>



<style>
    :global(.overlay) {
        position: fixed;
        top: 0;
        left: 0;
        width: 100vw;
        height: 100vh;
        background: rgba(0, 0, 0, 0.5);
        display: flex;
        justify-content: center;
        align-items: center;
        z-index: 1000;
        backdrop-filter: blur(
            0.25em
        ); 
    }

    :global(button) {
        display: inline-block;
        margin-top: 1rem;
        padding: 0.7rem 1.5rem;
        background-color: var(--third-color);
        color: var(--first-color);
        border: none;
        border-radius: 8px;
        font-size: 1rem;
        cursor: pointer;
        transition: all 0.5s ease;
    }

    :global(button:hover) {
        transform: scale(1.0125);
    }

    :global(.popup) {
        width: 80%;
        max-height: 80%;
        padding: 2rem;
        background-color: var(--first-color);
        border-radius: 1vw;
    }

    .container {
        padding: 1% 0.75%;
        display: flex;
        flex-direction: column;
        gap: 2vw;
    }

    .bold {
        font-weight: bold;
    }

    .section {
        align-self: center;
        display: flex;
        flex-direction: column;
        gap: 1vh;
        width: 80%;
        background-color: var(--fourth-color);
        border: 0.5rem solid var(--fourth-color);
        border-radius: 1vw;
        padding: 1.5rem;
        max-height: 77.5vh;
        overflow-y: scroll;
        transition: transform 0.3s ease;
        position: relative; /* Necessario per il positioning sticky */
    }

    /* Barretta di scorrimento trasparente */
    .section::-webkit-scrollbar {
        width: 12px;
        background: transparent; /* Rende il track di base invisibile */
    }

    .section:hover::-webkit-scrollbar-track {
        width: 0;
        height: 0;
    }

    .section:hover::-webkit-scrollbar-thumb {
        background-color: rgba(
            var(--second-color-rgb),
            0.5
        ); /* Thumb parzialmente trasparente */
        border-radius: 10px;
        border: 3px solid rgba(255, 255, 255, 0.3); /* Aggiunge spazio trasparente attorno al thumb */
        height: 20%;
    }
</style>
