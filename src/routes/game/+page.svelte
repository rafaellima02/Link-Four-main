<script>
  import Board from '$lib/component/board.svelte';
  import FirstFaller from '$lib/component/FirstFaller.svelte';
  import SecondFaller from '$lib/component/SecondFaller.svelte';
  import restart from '$lib/assets/Restart.svg';
  import flag from '$lib/assets/Flag.svg';
  import home from '$lib/assets/Vector.svg';

  function goHome() {
    console.log('clicou!');
    if (typeof window !== 'undefined') {
      window.location.href = '/';
    }
  }
</script>

<svelte:head>
  <link rel="stylesheet" href="/game.css" />
  <link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@1,800&display=swap" rel="stylesheet" />
</svelte:head>

<main class="home">
  <div class="container">
    <header class="top">

      <div class="logo-title">
        <div class="word">
          <div class="ball ball-red"></div>
          <span class="letter1">LINK</span>
        </div>
        <div class="word2">
          <span class="letter">FOUR</span>
          <div class="ball ball-yellow"></div>
        </div>
      </div>

      <button class="btn-home" onclick={goHome}>
        <img src={home} alt="Home Icon" />
        <span>home</span>
      </button>
    </header>

    <section class="game-content">
      <div class="game-turn">
        <div class="game-turn-bar">
          <p>Player 1's Turn</p>
        </div>
      </div>

      <div class="game-functions">
        <article class="player-card-1">
          <div class="player-avatar">
            <FirstFaller />
          </div>
          <p class="player-name">Player 1</p>
          <div class="player-score">
            <p class="player-score-label">Score</p>
            <p class="player1-score-value">0</p>
          </div>
        </article>

        <Board />

        <article class="player-card-2">
          <div class="player-avatar">
            <SecondFaller />
          </div>
          <p class="player-name">Player 2</p>
          <div class="player-score">
            <p class="player-score-label">Score</p>
            <p class="player2-score-value">0</p>
          </div>
        </article>
      </div>

      <footer class="game-options">
        <button class="btn btn-player-1">
          <img src={flag} alt="Flag Icon" />
          <span>FORFEIT</span>
        </button>
        <button class="btn-restart">
          <img src={restart} alt="Restart Icon" />
          <span>RESTART</span>
        </button>
        <button class="btn btn-player-2">
          <img src={flag} alt="Flag Icon" />
          <span>FORFEIT</span>
        </button>
      </footer>
    </section>
  </div>
</main>