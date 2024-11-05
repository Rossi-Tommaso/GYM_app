<script>
    let userName = "Utente"; // Cambia con il nome dell'utente se disponibile
  </script>
  
  <div class="homepage">
    <h1>Benvenuto, {userName}!</h1>
    <p class="welcome-text">
      Gestisci facilmente le tue schede di allenamento e il tuo piano alimentare per raggiungere i tuoi obiettivi.
    </p>
  
    <div class="sections">
      <div class="section">
        <h2>Allenamenti</h2>
        <p>Crea e personalizza le tue schede di allenamento.</p>
        <a href='/allenamenti' class="link">Vai agli Allenamenti</a>
      </div>
  
      <div class="section">
        <h2>Alimentazione</h2>
        <p>Gestisci il tuo piano alimentare per una dieta equilibrata.</p>
        <a href='/alimentazione' class="link">Vai alla Dieta</a>
      </div>
  
      <div class="section">
        <h2>Progressi</h2>
        <p>Tieni traccia dei tuoi risultati e migliora ogni giorno.</p>
        <a href='/progressi' class="link">Visualizza Progressi</a>
      </div>
  
      <div class="section">
        <h2>Consigli</h2>
        <p>Scopri suggerimenti per allenamenti e alimentazione.</p>
        <a href='/consigli' class="link">Scopri di più</a>
      </div>
    </div>
  </div>
  
  <style>
    :global(body) {
        margin: 0;
        padding: 0;
        height: 100vh;
        width: 100vw;
    }

    .homepage {
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 4vh;
      background: linear-gradient(to right, #ff7e5f, #feb47b);
      color: #fff;
      min-height: calc(100vh - 8vh);
    }
  
    h1 {
      font-size: 2.5rem;
      margin-bottom: 1vh;
    }
  
    .welcome-text {
      font-size: 1.2rem;
      margin-bottom: 8vh;
      text-align: center;
    }
  
    .sections {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1vw;
      min-width: 65vw;
      max-width: 75vw;
      min-height: 65vh;
      max-height: 75vh;
    }

    .section {
      background: rgba(255, 255, 255, 0.1);
      border-radius: 0.75rem;
      padding: 3vh 2vw;
      text-align: center;
      transition: transform 0.3s ease;
    }
  
    .section:hover {
      transform: scale(1.05);
    }
  
    .section h2 {
      font-size: 1.5rem;
      margin-bottom: 1vh;
    }
  
    .section p {
      font-size: 1rem;
      color: rgba(255, 255, 255, 0.8);
      margin-bottom: 2vh;
    }
  
    .link {
      display: inline-block;
      padding: 0.7em 1.5em;
      text-decoration: none;
      background-color: #fff;
      color: #ff7e5f;
      border-radius: 0.5rem;
      font-size: 1rem;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
  
    .link:hover {
      background-color: #f1f1f1;
    }
  </style>
  