<script>
  import { goto } from '$app/navigation';

 function goBack() {
    goto('/')
  }

   function goRules() {
    goto('/rules');
  }

  const team = [
    { name: 'Caio Santanna',     role: 'Designer',  icon: 'fa-brands fa-figma' },
    { name: 'João Ibson',        role: 'Designer',  icon: 'fa-brands fa-figma' },
    { name: 'Guilherme Santos',  role: 'Developer', icon: 'fa-solid fa-code' },
    { name: 'Daniel Henrique',   role: 'Developer', icon: 'fa-solid fa-code' },
    { name: 'Rafael Lima',       role: 'Developer', icon: 'fa-solid fa-code' }
  ];

  const technologies = [
    { name: 'FIGMA',      icon: 'fa-brands fa-figma' },
    { name: 'SVELTE',     icon: 'si si-svelte' },
    { name: 'HTML',       icon: 'fa-brands fa-html5' },
    { name: 'CSS',        icon: 'fa-brands fa-css3-alt' },
    { name: 'TYPESCRIPT', icon: 'si si-typescript' },
  ];
</script>

<svelte:head>
  <title>Credits – Connect Four</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.7.2/css/all.min.css" />
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/simple-icons-font@13/font/simple-icons.min.css" />
  <link rel="stylesheet" href="/credits.css" />
</svelte:head>

<main class="credits-page">

  <!-- NAV -->
  <nav id="NAV__prime0">
      <div id="DV_home_prime0">
        <button class="btn-voltar" onclick={goBack}>
          <img src="/icons/arrow.png" alt="logo" />
          BACK
        </button>
      </div>
    </nav>

  <!-- SIDEBAR -->
  <div class="credits-sidebar">
    <button class="btn-credits-active" onclick={goRules}>RULES</button>
    <button class="btn-credits-active">CREDITS</button>
  </div>

  <!-- CONTEÚDO PRINCIPAL -->
  <section class="credits-content">

    <div>
      <h1 class="credits-title">Credits</h1>
    </div>

    <h2 class="meet-title">Meet the team</h2>

    <!-- Team list -->
    <div class="team-panel">
      <div class="team-column">
        {#each team as member}
          <div class="member-card">
            <div class="member-avatar">
              <i class={member.icon}></i>
            </div>
            <div class="member-info">
              <span class="member-name">{member.name}</span>
              <span class="member-role">{member.role}</span>
            </div>
          </div>
        {/each}
      </div>
    </div>

    <!-- Technologies -->
    <h3 class="tech-title">Technologies</h3>
    <div class="tech-row">
      {#each technologies as tech}
        <div class="tech-item">
          <div class="tech-icon">
            <i class={tech.icon}></i>
          </div>
          <span class="tech-name">{tech.name}</span>
        </div>
      {/each}
    </div>

  </section>

</main>