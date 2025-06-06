<script>
  // For animated elements in the background
  let magicCircles = 1; // Number of large decorative circles
  let gridLines = 10; // Number of grid lines
  let sparks = 50; // Number of magical spark particles
</script>

<div
  class="fixed inset-0 w-full h-full -z-10 pointer-events-none overflow-hidden"
>
  <!-- Animated gradient background -->
  <div class="absolute inset-0 bg-[#18122B]">
    <!-- Magical circle -->
    <div
      class="absolute top-1/4 right-1/4 w-[32rem] h-[32rem] opacity-70 animate-spin-slow drop-shadow-[0_0_60px_#ff79c6]"
    >
      <div
        class="absolute inset-0 rounded-full border-4 border-pink-400/80 blur-[2px]"
      ></div>
      <div
        class="absolute inset-4 rounded-full border-4 border-purple-400/80 blur-[2px]"
      ></div>
      <div
        class="absolute inset-8 rounded-full border-4 border-pink-400/80 blur-[2px]"
      ></div>
      <!-- Magic runes -->
      {#each Array(12) as _, i}
        <div
          class="absolute w-7 h-7 text-pink-400 animate-glow"
          style="
            left: 50%;
            top: 50%;
            transform: rotate({i * 30}deg) translateY(-200px) rotate(-{i *
            30}deg);
            text-shadow: 0 0 16px #ff79c6, 0 0 8px #bd93f9;
          "
        >
          ★
        </div>
      {/each}
    </div>

    <!-- Main gradients -->
    <div
      class="absolute inset-0 opacity-90 bg-gradient-radial from-pink-500/60 via-purple-600/40 to-transparent animate-pulse blur-[2px]"
    ></div>
    <div
      class="absolute inset-0 opacity-80 bg-[radial-gradient(circle_at_60%_40%,rgba(255,121,198,0.5),rgba(189,147,249,0.3),transparent_80%)] animate-pulse-slow blur-[1.5px]"
    ></div>

    <!-- Cyberpunk-anime grid -->
    <div
      class="absolute inset-0 bg-[linear-gradient(transparent_1.5px,transparent_1.5px),linear-gradient(90deg,rgba(255,121,198,0.4)_1.5px,transparent_1.5px)] bg-[length:32px_32px] opacity-70"
    ></div>

    <!-- Energy field effect -->
    <div
      class="absolute inset-0 bg-gradient-to-t from-pink-400/30 via-transparent to-purple-400/30 animate-pulse-slow blur-[1px]"
    ></div>

    <!-- Magical sparks -->
    {#each Array(sparks) as _, i}
      <div
        class="absolute rounded-full bg-gradient-to-r from-pink-400 to-purple-400 animate-magic-spark"
        style="
          left: {Math.random() * 100}%;
          top: {Math.random() * 100}%;
          width: {4 + Math.random() * 6}px;
          height: {4 + Math.random() * 6}px;
          animation-delay: -{Math.random() * 5}s;
          animation-duration: {3 + Math.random() * 4}s;
          opacity: 0.95;
          box-shadow: 0 0 18px #ff79c6, 0 0 8px #bd93f9;
        "
      ></div>
    {/each}

    <!-- Power lines -->
    {#each Array(3) as _, i}
      <div
        class="absolute h-full w-[4px] bg-gradient-to-b from-transparent via-pink-400/90 to-transparent animate-power-surge blur-[1px]"
        style="
          left: {20 + i * 30}%;
          animation-delay: -{i * 0.5}s;
          box-shadow: 0 0 18px #ff79c6;
        "
      ></div>
    {/each}
  </div>

  <!-- Decorative lines -->
  <div class="absolute inset-0 overflow-hidden">
    {#each Array(8) as _, i}
      <div
        class="absolute h-[3px] bg-gradient-to-r from-transparent via-pink-500/80 to-transparent w-full transform animate-slide-right blur-[1px]"
        style="
          top: {10 + i * 12}%;
          animation-delay: -{Math.random() * 5}s;
          animation-duration: {20 + Math.random() * 10}s;
        "
      ></div>
    {/each}
    {#each Array(5) as _, i}
      <div
        class="absolute w-[3px] bg-gradient-to-b from-transparent via-purple-500/80 to-transparent h-full transform animate-slide-down blur-[1px]"
        style="
          left: {15 + i * 20}%;
          animation-delay: -{Math.random() * 5}s;
          animation-duration: {15 + Math.random() * 10}s;
        "
      ></div>
    {/each}
  </div>
</div>

<style>
  @keyframes slide-right {
    from {
      transform: translateX(-100%);
    }
    to {
      transform: translateX(100%);
    }
  }

  @keyframes slide-down {
    from {
      transform: translateY(-100%);
    }
    to {
      transform: translateY(100%);
    }
  }

  @keyframes float-particle {
    0% {
      transform: translate(0, 0) rotate(0deg);
      opacity: 0;
      filter: blur(1px);
    }
    20% {
      opacity: 1;
      filter: blur(0px);
    }
    80% {
      opacity: 1;
      filter: blur(0px);
    }
    100% {
      transform: translate(var(--move-x, 100px), var(--move-y, 100px))
        rotate(360deg);
      opacity: 0;
      filter: blur(1px);
    }
  }

  @keyframes magic-spark {
    0% {
      transform: scale(0) rotate(0deg);
      opacity: 0;
    }
    50% {
      opacity: 1;
    }
    100% {
      transform: scale(2) rotate(180deg);
      opacity: 0;
    }
  }

  @keyframes power-surge {
    0% {
      opacity: 0;
      transform: scaleY(0);
    }
    50% {
      opacity: 1;
      transform: scaleY(1);
    }
    100% {
      opacity: 0;
      transform: scaleY(0);
    }
  }

  @keyframes glow {
    0%,
    100% {
      opacity: 0.3;
      filter: blur(2px);
    }
    50% {
      opacity: 1;
      filter: blur(1px);
    }
  }

  .animate-slide-right {
    animation: slide-right 15s linear infinite;
  }

  .animate-slide-down {
    animation: slide-down 15s linear infinite;
  }

  .animate-float-particle {
    --move-x: 150px;
    --move-y: 150px;
    animation: float-particle 10s linear infinite;
  }

  .animate-pulse-slow {
    animation: pulse 4s cubic-bezier(0.4, 0, 0.6, 1) infinite;
  }

  .animate-spin-slow {
    animation: spin 20s linear infinite;
  }

  .animate-glow {
    animation: glow 2s ease-in-out infinite;
  }

  .animate-magic-spark {
    animation: magic-spark 3s ease-out infinite;
  }
</style>
