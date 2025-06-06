<script>
  // Number of particles for floating particle effect
  let particles = Array(15).fill(null);
</script>

<section id="features" class="py-20 bg-slate-900/95 relative overflow-hidden">
  <!-- Cyberpunk grid background -->
  <div
    class="absolute inset-0 bg-[linear-gradient(transparent_1px,transparent_1px),linear-gradient(90deg,rgba(189,147,249,0.2)_1px,transparent_1px)] bg-[length:20px_20px] opacity-20 pointer-events-none"
  ></div>

  <!-- Floating particles -->
  <div class="absolute inset-0 pointer-events-none">
    {#each particles as _, i}
      <div
        class="absolute rounded-full bg-gradient-to-r from-pink-400/40 to-purple-400/40 animate-particle-float"
        style="
          left: {Math.random() * 100}%;
          top: {Math.random() * 100}%;
          width: {3 + Math.random() * 4}px;
          height: {3 + Math.random() * 4}px;
          box-shadow: 0 0 8px rgba(255, 121, 198, 0.5);
          animation-delay: -{Math.random() * 10}s;
          animation-duration: {15 + Math.random() * 15}s;
        "
      ></div>
    {/each}
  </div>

  <div class="container mx-auto px-6 relative z-10">
    <!-- Section Header with glowing title and decorative elements -->
    <div class="relative text-center mb-16 animate-fade-in">
      <div
        class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-32 h-32 bg-purple-500/20 rounded-full blur-3xl"
      ></div>
      <h2
        class="text-4xl font-bold text-purple-400 cyber-text-glow mb-6 relative"
      >
        機能<span class="text-pink-400 ml-3">Features</span>
      </h2>
      <div
        class="w-48 h-1 mx-auto mt-4 bg-gradient-to-r from-transparent via-purple-400 to-transparent"
      ></div>
      <p class="text-gray-300 max-w-3xl mx-auto text-lg mt-8">
        Windows gaming on macOS with seamless integration
      </p>
    </div>

    <!-- Features Grid -->
    <div
      class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 max-w-6xl mx-auto stagger-children"
    >
      <!-- Game Library Management -->
      <div class="cyber-card">
        <!-- Decorative corner -->
        <div
          class="absolute top-0 left-0 w-8 h-8 border-t-2 border-l-2 border-pink-400/30 hover:border-pink-400 transition-colors duration-300"
        ></div>
        <div
          class="absolute bottom-0 right-0 w-8 h-8 border-b-2 border-r-2 border-pink-400/30 hover:border-pink-400 transition-colors duration-300"
        ></div>

        <div class="relative">
          <div
            class="absolute inset-0 text-3xl text-pink-400 blur-sm hover:blur-md transition-all duration-300"
          >
            <i class="fas fa-gamepad"></i>
          </div>
          <div
            class="relative text-3xl text-pink-400 hover:text-pink-300 transition-colors duration-300"
          >
            <i class="fas fa-gamepad"></i>
          </div>
        </div>

        <h3 class="text-lg font-semibold text-purple-300 mt-4 mb-3">
          Game Library
        </h3>
        <p class="text-gray-300 mb-4">
          Organize and manage your Windows game collection with intuitive
          one-click launch system
        </p>

        <!-- Anime-style divider -->
        <div class="relative h-1 mt-auto">
          <div
            class="absolute inset-0 bg-gradient-to-r from-transparent via-pink-400/50 to-transparent opacity-0 hover:opacity-100 transition-opacity duration-500"
          ></div>
        </div>
      </div>

      <!-- Wine & GPTK Integration -->
      <div class="cyber-card">
        <!-- Decorative corner -->
        <div
          class="absolute top-0 left-0 w-8 h-8 border-t-2 border-l-2 border-purple-400/30 hover:border-purple-400 transition-colors duration-300"
        ></div>
        <div
          class="absolute bottom-0 right-0 w-8 h-8 border-b-2 border-r-2 border-purple-400/30 hover:border-purple-400 transition-colors duration-300"
        ></div>

        <div class="relative">
          <div
            class="absolute inset-0 text-3xl text-purple-400 blur-sm hover:blur-md transition-all duration-300"
          >
            <i class="fas fa-wine-glass"></i>
          </div>
          <div
            class="relative text-3xl text-purple-400 hover:text-purple-300 transition-colors duration-300"
          >
            <i class="fas fa-wine-glass"></i>
          </div>
        </div>

        <h3 class="text-lg font-semibold text-pink-300 mt-4 mb-3">
          GPTK Integration
        </h3>
        <p class="text-gray-300 mb-4">
          Apple Silicon optimized gaming with seamless Wine and Game Porting
          Toolkit integration
        </p>

        <!-- Anime-style divider -->
        <div class="relative h-1 mt-auto">
          <div
            class="absolute inset-0 bg-gradient-to-r from-transparent via-purple-400/50 to-transparent opacity-0 hover:opacity-100 transition-opacity duration-500"
          ></div>
        </div>
      </div>

      <!-- Native macOS Experience -->
      <div class="cyber-card">
        <!-- Decorative corner -->
        <div
          class="absolute top-0 left-0 w-8 h-8 border-t-2 border-l-2 border-cyan-400/30 hover:border-cyan-400 transition-colors duration-300"
        ></div>
        <div
          class="absolute bottom-0 right-0 w-8 h-8 border-b-2 border-r-2 border-cyan-400/30 hover:border-cyan-400 transition-colors duration-300"
        ></div>

        <div class="relative">
          <div
            class="absolute inset-0 text-3xl text-cyan-400 blur-sm hover:blur-md transition-all duration-300"
          >
            <i class="fab fa-apple"></i>
          </div>
          <div
            class="relative text-3xl text-cyan-400 hover:text-cyan-300 transition-colors duration-300"
          >
            <i class="fab fa-apple"></i>
          </div>
        </div>

        <h3 class="text-lg font-semibold text-purple-300 mt-4 mb-3">
          Native Experience
        </h3>
        <p class="text-gray-300 mb-4">
          True macOS integration with native window management and system
          controls
        </p>

        <!-- Anime-style divider -->
        <div class="relative h-1 mt-auto">
          <div
            class="absolute inset-0 bg-gradient-to-r from-transparent via-cyan-400/50 to-transparent opacity-0 hover:opacity-100 transition-opacity duration-500"
          ></div>
        </div>
      </div>

      <!-- Performance Optimization -->
      <div class="cyber-card">
        <!-- Decorative corner -->
        <div
          class="absolute top-0 left-0 w-8 h-8 border-t-2 border-l-2 border-pink-400/30 hover:border-pink-400 transition-colors duration-300"
        ></div>
        <div
          class="absolute bottom-0 right-0 w-8 h-8 border-b-2 border-r-2 border-pink-400/30 hover:border-pink-400 transition-colors duration-300"
        ></div>

        <div class="relative">
          <div
            class="absolute inset-0 text-3xl text-pink-400 blur-sm hover:blur-md transition-all duration-300"
          >
            <i class="fas fa-bolt"></i>
          </div>
          <div
            class="relative text-3xl text-pink-400 hover:text-pink-300 transition-colors duration-300"
          >
            <i class="fas fa-bolt"></i>
          </div>
        </div>

        <h3 class="text-lg font-semibold text-purple-300 mt-4 mb-3">
          Performance
        </h3>
        <p class="text-gray-300 mb-4">
          Optimized for Apple Silicon with hardware acceleration for maximum
          gaming performance
        </p>

        <!-- Anime-style divider -->
        <div class="relative h-1 mt-auto">
          <div
            class="absolute inset-0 bg-gradient-to-r from-transparent via-pink-400/50 to-transparent opacity-0 hover:opacity-100 transition-opacity duration-500"
          ></div>
        </div>
      </div>

      <!-- Easy Setup -->
      <div class="cyber-card">
        <!-- Decorative corner -->
        <div
          class="absolute top-0 left-0 w-8 h-8 border-t-2 border-l-2 border-purple-400/30 hover:border-purple-400 transition-colors duration-300"
        ></div>
        <div
          class="absolute bottom-0 right-0 w-8 h-8 border-b-2 border-r-2 border-purple-400/30 hover:border-purple-400 transition-colors duration-300"
        ></div>

        <div class="relative">
          <div
            class="absolute inset-0 text-3xl text-purple-400 blur-sm hover:blur-md transition-all duration-300"
          >
            <i class="fas fa-wrench"></i>
          </div>
          <div
            class="relative text-3xl text-purple-400 hover:text-purple-300 transition-colors duration-300"
          >
            <i class="fas fa-wrench"></i>
          </div>
        </div>

        <h3 class="text-lg font-semibold text-pink-300 mt-4 mb-3">
          Easy Setup
        </h3>
        <p class="text-gray-300 mb-4">
          Simplified installation and configuration process with automatic
          environment setup
        </p>

        <!-- Anime-style divider -->
        <div class="relative h-1 mt-auto">
          <div
            class="absolute inset-0 bg-gradient-to-r from-transparent via-purple-400/50 to-transparent opacity-0 hover:opacity-100 transition-opacity duration-500"
          ></div>
        </div>
      </div>

      <!-- Community Support -->
      <div class="cyber-card">
        <!-- Decorative corner -->
        <div
          class="absolute top-0 left-0 w-8 h-8 border-t-2 border-l-2 border-cyan-400/30 hover:border-cyan-400 transition-colors duration-300"
        ></div>
        <div
          class="absolute bottom-0 right-0 w-8 h-8 border-b-2 border-r-2 border-cyan-400/30 hover:border-cyan-400 transition-colors duration-300"
        ></div>

        <div class="relative">
          <div
            class="absolute inset-0 text-3xl text-cyan-400 blur-sm hover:blur-md transition-all duration-300"
          >
            <i class="fab fa-github"></i>
          </div>
          <div
            class="relative text-3xl text-cyan-400 hover:text-cyan-300 transition-colors duration-300"
          >
            <i class="fab fa-github"></i>
          </div>
        </div>

        <h3 class="text-lg font-semibold text-purple-300 mt-4 mb-3">
          Open Source
        </h3>
        <p class="text-gray-300 mb-4">
          Free and open source software with active community development and
          support
        </p>

        <!-- Anime-style divider -->
        <div class="relative h-1 mt-auto">
          <div
            class="absolute inset-0 bg-gradient-to-r from-transparent via-cyan-400/50 to-transparent opacity-0 hover:opacity-100 transition-opacity duration-500"
          ></div>
        </div>
      </div>
    </div>

    <!-- Call to Action -->
    <div
      class="mt-20 text-center animate-slide-up"
      style="animation-delay: 0.6s;"
    >
      <div
        class="inline-flex items-center gap-4 py-4 px-8 bg-slate-800/70 backdrop-blur-sm"
      >
        <div class="w-3 h-3 bg-pink-500 rounded-full animate-pulse-glow"></div>
        <p class="text-lg text-gray-300">
          Ready to elevate your macOS gaming experience? <span
            class="text-pink-400">kimiz</span
          > awaits.
        </p>
      </div>
      <div class="flex justify-center gap-6 mt-8">
        <a
          href="https://github.com/lidl-dev/kimiz"
          class="button-primary"
          target="_blank"
          rel="noopener"
        >
          <i
            class="fa-brands fa-github mr-2 hover:rotate-12 transition-transform duration-300"
          ></i>
          Explore on GitHub
        </a>
      </div>
    </div>
  </div>

  <!-- Decorative corner accents for entire section -->
  <div
    class="absolute top-0 left-0 w-32 h-32 border-t-2 border-l-2 border-purple-400/10 hidden lg:block"
  ></div>
  <div
    class="absolute bottom-0 right-0 w-32 h-32 border-b-2 border-r-2 border-pink-400/10 hidden lg:block"
  ></div>
</section>
