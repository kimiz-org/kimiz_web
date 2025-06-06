<script lang="ts">
  import Sakura from "./Sakura.svelte";

  // For particle effects
  let particles = Array(40).fill(null);
</script>

<!-- Sakura petals overlay -->
<Sakura />

<section
  class="min-h-screen flex items-center justify-center pt-20 bg-anime-bg relative overflow-hidden"
>
  <!-- Cyberpunk grid background -->
  <div
    class="absolute inset-0 bg-[linear-gradient(transparent_1px,transparent_1px),linear-gradient(90deg,rgba(189,147,249,0.3)_1px,transparent_1px)] bg-[length:20px_20px] opacity-30 pointer-events-none"
  ></div>

  <!-- Floating particles -->
  <div class="absolute inset-0 pointer-events-none">
    {#each particles as _, i}
      <div
        class="absolute rounded-full bg-gradient-to-r from-pink-400/50 to-purple-400/50 animate-particle-float"
        style="
          left: {Math.random() * 100}%;
          top: {Math.random() * 100}%;
          width: {5 + Math.random() * 5}px;
          height: {5 + Math.random() * 5}px;
          box-shadow: 0 0 8px rgba(255, 121, 198, 0.6);
          animation-delay: -{Math.random() * 10}s;
          animation-duration: {20 + Math.random() * 20}s;
        "
      ></div>
    {/each}
  </div>

  <!-- Main Content -->
  <div class="container mx-auto px-6 text-center max-w-4xl relative z-10">
    <!-- Header with glow effect -->
    <div class="mb-12 animate-fade-in">
      <div class="relative">
        <!-- Magic circle background -->
        <div
          class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-48 h-48 opacity-20"
        >
          <svg viewBox="0 0 200 200" class="w-full h-full animate-spin-slow">
            <circle
              cx="100"
              cy="100"
              r="80"
              fill="none"
              stroke="url(#magic-gradient)"
              stroke-width="1"
              stroke-dasharray="5,5"
            />
            <circle
              cx="100"
              cy="100"
              r="60"
              fill="none"
              stroke="url(#magic-gradient)"
              stroke-width="0.5"
              stroke-dasharray="3,3"
            />
            <circle
              cx="100"
              cy="100"
              r="40"
              fill="none"
              stroke="url(#magic-gradient)"
              stroke-width="0.5"
            />
            <defs>
              <linearGradient
                id="magic-gradient"
                x1="0%"
                y1="0%"
                x2="100%"
                y2="100%"
              >
                <stop offset="0%" style="stop-color:#ff79c6;stop-opacity:1" />
                <stop offset="50%" style="stop-color:#bd93f9;stop-opacity:1" />
                <stop offset="100%" style="stop-color:#8be9fd;stop-opacity:1" />
              </linearGradient>
            </defs>
          </svg>
        </div>

        <div
          class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-32 h-32 bg-pink-500/20 rounded-full blur-3xl"
        ></div>
        <h1
          class="text-5xl md:text-6xl font-bold text-pink-400 mb-6 cyber-text-glow relative z-10"
        >
          kimiz
        </h1>
      </div>
      <p class="text-xl text-purple-300">Run Windows games on macOS</p>
    </div>

    <!-- Main Description -->
    <div class="mb-16 animate-slide-up" style="animation-delay: 0.2s;">
      <div class="relative inline-block">
        <div
          class="absolute -inset-1 bg-gradient-to-r from-pink-600/20 to-purple-600/20 rounded-lg blur-sm"
        ></div>
        <p
          class="relative text-lg text-gray-300 max-w-3xl mx-auto leading-relaxed bg-slate-900/30 backdrop-blur-sm px-8 py-4"
        >
          Run your favorite <span class="text-pink-400 font-semibold"
            >Windows games</span
          >
          on macOS using
          <span class="text-cyan-400 font-semibold">Wine</span> and
          <span class="text-purple-400 font-semibold">Game Porting Toolkit</span
          > integration. Simple setup, native performance.
        </p>
      </div>
    </div>

    <!-- Call to Action -->
    <div
      class="flex flex-col sm:flex-row gap-6 justify-center items-center mb-20 animate-slide-up"
      style="animation-delay: 0.4s;"
    >
      <a
        href="https://github.com/kimiz-org/kimiz"
        class="hero-icon-btn"
        target="_blank"
        rel="noopener"
        aria-label="GitHub"
      >
        <i class="fa-brands fa-github mr-2"></i>
        <span class=" sm:inline">View on GitHub</span>
      </a>
      <a href="#features" class="hero-icon-btn" aria-label="Learn More">
        <i class="fa-solid fa-arrow-down mr-2"></i>
        <span class=" sm:inline">Learn More</span>
      </a>
    </div>

    <!-- Feature Highlights -->
    <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-16 stagger-children">
      <div class="cyber-card">
        <div
          class="absolute top-0 right-0 w-1 h-1 bg-pink-400 rounded-full hover:animate-ping"
        ></div>
        <div class="relative">
          <div
            class="relative text-3xl text-pink-400 hover:text-pink-300 transition-colors duration-300"
          >
            <i class="fa-solid fa-gamepad"></i>
          </div>
        </div>
        <h3 class="text-lg font-semibold text-purple-300 mt-4 mb-3">
          Gaming Excellence
        </h3>
        <p class="text-gray-300">
          Seamless Windows game compatibility with native macOS integration
        </p>
      </div>

      <div class="cyber-card">
        <div
          class="absolute top-0 right-0 w-1 h-1 bg-purple-400 rounded-full hover:animate-ping"
        ></div>
        <div class="relative">
          <div
            class="relative text-3xl text-purple-400 hover:text-purple-300 transition-colors duration-300"
          >
            <i class="fa-solid fa-bolt"></i>
          </div>
        </div>
        <h3 class="text-lg font-semibold text-pink-300 mt-4 mb-3">
          Native Performance
        </h3>
        <p class="text-gray-300">
          Optimized for Apple Silicon with hardware acceleration
        </p>
      </div>

      <div class="cyber-card">
        <div
          class="absolute top-0 right-0 w-1 h-1 bg-cyan-400 rounded-full group-hover:animate-ping"
        ></div>
        <div class="relative">
          <div
            class="relative text-3xl text-cyan-400 group-hover:text-cyan-300 transition-colors duration-300"
          >
            <i class="fa-solid fa-wrench"></i>
          </div>
        </div>
        <h3 class="text-lg font-semibold text-purple-300 mt-4 mb-3">
          Easy Setup
        </h3>
        <p class="text-gray-300">
          One-click Wine configuration and game installation
        </p>
      </div>
    </div>

    <!-- Status Badge -->
    <div
      class="inline-flex items-center gap-3 bg-slate-800/70 backdrop-blur-sm border border-pink-400/20 px-6 py-3 rounded-full shadow-sm animate-slide-up"
      style="animation-delay: 0.8s;"
    >
      <div class="w-2 h-2 bg-pink-500 rounded-full animate-pulse-glow"></div>
      <span class="text-sm text-gray-300">
        In Development • Open Source• Apple Silicon Ready
      </span>
    </div>

    <!-- Decorative corner accents -->
    <div
      class="absolute top-0 left-0 w-32 h-32 border-t-2 border-l-2 border-purple-400/30 -translate-x-1 -translate-y-1 hidden md:block"
    ></div>
    <div
      class="absolute bottom-0 right-0 w-32 h-32 border-b-2 border-r-2 border-pink-400/30 translate-x-1 translate-y-1 hidden md:block"
    ></div>
  </div>
</section>

<style>
  .hero-icon-btn {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    min-width: 2.75rem;
    min-height: 2.75rem;
    padding: 0.75rem 1.5rem;
    border-radius: 0.75rem;
    background: rgba(30, 27, 54, 0.7);
    border: 2px solid rgba(255, 121, 198, 0.25);
    color: #ff79c6;
    font-size: 1.15rem;
    font-weight: 500;
    box-shadow: 0 0 12px 0 rgba(255, 121, 198, 0.12);
    transition:
      border-color 0.2s,
      color 0.2s,
      box-shadow 0.2s,
      background 0.2s;
    overflow: hidden;
    z-index: 1;
    gap: 0.5rem;
    text-decoration: none;
  }
  .hero-icon-btn:hover,
  .hero-icon-btn:focus {
    border-color: #bd93f9;
    color: #bd93f9;
    background: linear-gradient(
      90deg,
      rgba(255, 121, 198, 0.12) 0%,
      rgba(189, 147, 249, 0.12) 100%
    );
    box-shadow:
      0 0 18px 0 #bd93f9,
      0 0 8px 0 #ff79c6;
    outline: none;
  }
  .hero-icon-btn:active {
    border-color: #8be9fd;
    color: #8be9fd;
    background: linear-gradient(
      90deg,
      rgba(139, 233, 253, 0.18) 0%,
      rgba(255, 121, 198, 0.18) 100%
    );
    box-shadow: 0 0 10px 0 #8be9fd;
  }
</style>
