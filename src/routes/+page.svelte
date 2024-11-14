<script>
    let utente = "Utente";
</script>

<div class="container">
    <h1 class="welcome anton-sc-regular">Welcome to Fit Tracker {utente}</h1>
    <div class="blocks-container">
        <div class="section">
            <h2 class="faculty-glyphic-regular">Allenamenti</h2>
            <p class="faculty-glyphic-regular">Crea e personalizza le tue schede di allenamento.</p>
            <a href="/allenamenti" class="anton-sc-regular">Vai agli Allenamenti</a>
        </div>

        <div class="section">
            <h2 class="faculty-glyphic-regular">Alimentazione</h2>
            <p class="faculty-glyphic-regular">Gestisci il tuo piano alimentare per una dieta equilibrata.</p>
            <a href="/alimentazione" class="anton-sc-regular">Vai alla Dieta</a>
        </div>

        <div class="section">
            <h2 class="faculty-glyphic-regular">Progressi</h2>
            <p class="faculty-glyphic-regular">Tieni traccia dei tuoi risultati e migliora ogni giorno.</p>
            <a href="/progressi" class="anton-sc-regular">Visualizza Progressi</a>
        </div>

        <div class="section">
            <h2 class="faculty-glyphic-regular">Consigli</h2>
            <p class="faculty-glyphic-regular">Scopri suggerimenti per allenamenti e alimentazione.</p>
            <a href="/consigli" class="anton-sc-regular">Scopri di più</a>
        </div>
    </div>
</div>

<style>
    .container {
        padding: 1% 0.75%;
        display: flex;
        flex-direction: column;
        gap: 2vw;
    }

    .welcome {
        margin-left: 2vw;
        font-size: 2.5em;
        color: var(--second-color);
    }

    .blocks-container {
        align-self: center;
        justify-self: center;
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        width: 72.5%;
        aspect-ratio: 18/9;
        gap: 1.5vw;
    }

    .section {
        display: flex;
        flex-direction: column;
        background-color: var(--fourth-color);
        border-radius: 1vw;
        padding: 1.5rem;
        justify-content: space-evenly;
        transition: transform 0.3s ease;
    }

    .section:hover {
        transform: scale(1.05);
    }

    .section h2 {
        font-size: 1.5rem;
        margin-bottom: 0.5rem;
        color: var(--second-color);
    }

    .section p {
        font-size: 1rem;
        color: var(--third-color);
    }

    .section a {
        margin-top: 1rem;
        padding: 0.7rem 1.5rem;
        background-color: var(--third-color);
        color: var(--first-color);
        text-decoration: none;
        border: none;
        border-radius: 8px;
        font-size: 1rem;
        cursor: pointer;
        transition: all 0.5s ease;
    }

    .section a:hover {
        color: var(--third-color);
        background-color: var(--first-color);
        transform: scale(1.01);
    }
</style>
