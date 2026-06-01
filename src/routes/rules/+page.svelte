<script>
  function goBack() {
    if (typeof window !== 'undefined') {
      history.back();
    }
  }

  function handleRules() {
    console.log('Rules clicked');
  }

  function handleCredits() {
    console.log('Credits clicked');
  }
</script>

<svelte:head>
  <title>Link Four</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.7.2/css/all.min.css" />
  <link rel="stylesheet" href="/rules.css" />
</svelte:head>

<main class="home">
  <div id="page">

    <nav id="NAV__prime0">
      <div id="DV_home_prime0">
        <button class="btn-voltar" on:click={goBack}>
          <img src="/icons/arrow.png" alt="logo" />
          BACK
        </button>
      </div>
    </nav>

    <div class="titulo">
      <h1>Rules of</h1>
      <h2>Game</h2>
    </div>

    <div id="DV_regras_e_creditos">
      <button class="A_regras_e_creditos" on:click={handleRules}>
        <i class="fa-solid fa-circle-info"></i>
        RULES
      </button>

      <button class="A_regras_e_creditos" on:click={handleCredits}>
        <i class="fa-regular fa-star"></i>
        CREDITS
      </button>
    </div>

    <section id="SEC_prime0">
      <div class="DV_main_card">
        <div class="DV_card_content">

          <div class="DV__board">
            <!-- LINHA 1 -->
            <div class="slot"></div>
            <div class="slot"></div>
            <div class="slot"></div>
            <div class="slot"></div>
            <div class="slot"></div>

            <!-- LINHA 2 -->
            <div class="slot"></div>
            <div class="slot"></div>
            <div class="slot"></div>
            <div class="slot"></div>
            <div class="slot"></div>

            <!-- LINHA 3 -->
            <div class="slot"></div>
            <div class="slot"></div>
            <div class="slot red"></div>
            <div class="slot"></div>
            <div class="slot"></div>

            <!-- LINHA 4 -->
            <div class="slot"></div>
            <div class="slot red"></div>
            <div class="slot red"></div>
            <div class="slot yellow"></div>
            <div class="slot"></div>

            <!-- LINHA 5 -->
            <div class="slot red"></div>
            <div class="slot yellow"></div>
            <div class="slot red"></div>
            <div class="slot red"></div>
            <div class="slot yellow"></div>
          </div>

          <div class="DV_text_area">
            <h2>
              Link Four is a classic strategy game for players of all ages!
            </h2>
            <p>
              Your objective is simple: connect 4 pieces of your color in a row before your opponent.
              Create horizontal, vertical, or diagonal lines, plan your strategy, and claim victory!
            </p>
          </div>

        </div>
      </div>
    </section>

    <section id="SEC__prime1">
      <div class="DV_resumo_prime0">
        <i class="fa-solid fa-brain"></i>
        <h3>STRATEGY</h3>
        <p>Every move counts. Plan your actions and outsmart your opponent.</p>
      </div>

      <div class="DV_resumo_prime0">
        <i class="fa-solid fa-users"></i>
        <h3>FOR EVERYONE</h3>
        <p>Guaranteed fun for all ages. Play with friends or challenge the AI.</p>
      </div>

      <div class="DV_resumo_prime0">
        <i class="fa-solid fa-trophy"></i>
        <h3>CHALLENGE YOURSELF</h3>
        <p>Improve your skills and become the master of Four in a Row.</p>
      </div>
    </section>

  </div>
</main>
