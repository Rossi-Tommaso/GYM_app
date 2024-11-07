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
        color: #0c1618;
    }

    .blocks-container {
        align-self: center;
        justify-self: center;
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        width: 75%;
        aspect-ratio: 18/9;
        gap: 1.5vw;
    }

    .section {
        display: flex;
        flex-direction: column;
        background-color: rgba(70, 19, 2, 0.1);
        border-radius: 12px;
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
        color: #0c1618;
    }

    .section p {
        font-size: 1rem;
        color: #462418;
    }

    .section a {
        margin-top: 1rem;
        padding: 0.7rem 1.5rem;
        background-color: #6B2B06;
        color: #F4D6CC;
        text-decoration: none;
        border: none;
        border-radius: 8px;
        font-size: 1rem;
        cursor: pointer;
        transition: all 0.5s ease;
    }

    .section a:hover {
        color: #6B2B06;
        background-color: #F4D6CC;
        transform: scale(1.01);
    }
</style>
