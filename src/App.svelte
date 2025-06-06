<script lang="ts">
  import Hero from "./lib/components/Hero.svelte";
  import Features from "./lib/components/Features.svelte";
  import Footer from "./lib/components/Footer.svelte";
  import AnimeBg from "./lib/components/AnimeBg.svelte";
</script>

<svelte:head>
  <title>kimiz - Windows Gaming on macOS</title>
  <meta
    name="description"
    content="Run Windows games seamlessly on macOS with kimiz - powered by Wine and Game Porting Toolkit integration"
  />
  <meta
    name="keywords"
    content="macOS gaming, Windows games, Wine, Game Porting Toolkit, GPTK, Apple Silicon"
  />
  <meta name="author" content="lidl.dev" />

  <!-- Open Graph / Facebook -->
  <meta property="og:type" content="website" />
  <meta property="og:url" content="https://kimiz.lidl.dev/" />
  <meta property="og:title" content="kimiz - Windows Gaming on macOS" />
  <meta
    property="og:description"
    content="Run Windows games seamlessly on macOS with kimiz - powered by Wine and Game Porting Toolkit integration"
  />

  <!-- Twitter -->
  <meta property="twitter:card" content="summary_large_image" />
  <meta property="twitter:url" content="https://kimiz.lidl.dev/" />
  <meta property="twitter:title" content="kimiz - Windows Gaming on macOS" />
  <meta
    property="twitter:description"
    content="Run Windows games seamlessly on macOS with kimiz - powered by Wine and Game Porting Toolkit integration"
  />
</svelte:head>

<main class="relative">
  <!-- Apply cyberpunk/anime background -->
  <AnimeBg />

  <Hero />
  <Features />
</main>

<Footer />

<style>
  :global(html) {
    scroll-behavior: smooth;
  }

  :global(body) {
    margin: 0;
    padding: 0;
    background-color: var(--anime-bg);
    min-height: 100vh;
    color: var(--text-primary);
    font-family:
      "Poppins",
      -apple-system,
      BlinkMacSystemFont,
      sans-serif;
    position: relative;
    overflow-x: hidden;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }

  @keyframes subtle-shimmer {
    0% {
      background-position: 0% 0%;
    }
    100% {
      background-position: 100% 100%;
    }
  }

  :global(#app) {
    min-height: 100vh;
  }
</style>
