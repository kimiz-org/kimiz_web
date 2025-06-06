<script>
  // For simple floating petals effect
  let petals = Array(30).fill(null);

  // Detect if mobile for responsive design
  let isMobile = false;

  if (typeof window !== "undefined") {
    isMobile = window.innerWidth < 768;
  }
</script>

<div
  class="fixed inset-0 w-full h-full z-0 pointer-events-none overflow-hidden"
>
  {#each petals as _, i}
    <div
      class="absolute top-0 animate-float"
      style="
        left: {Math.random() * 100}%;
        animation-delay: -{Math.random() * 20}s;
        animation-duration: {(isMobile ? 10 : 15) + Math.random() * 10}s;
        will-change: transform;
        z-index: 0;
      "
    >
      <div
        class="bg-gradient-to-br from-pink-300/95 to-pink-400/90 rotate-45 rounded-tl-full rounded-br-full animate-neon-glow blur-[1.5px] shadow-sakura"
        style="
          width: {isMobile ? 14 : 28}px;
          height: {isMobile ? 12 : 24}px;
          opacity: 0.85;
          box-shadow: 0 0 {isMobile ? 18 : 36}px #ff79c6, 0 0 8px #fff2fa;
        "
      ></div>
    </div>
  {/each}
</div>

<style>
  @keyframes float {
    0% {
      transform: translateY(-10%) translateX(0) rotate(0deg) scale(0.8);
      opacity: 0;
    }
    10% {
      opacity: 1;
      transform: translateY(5vh) translateX(10px) rotate(36deg) scale(1);
    }
    25% {
      transform: translateY(25vh) translateX(30px) rotate(90deg) scale(1.1);
    }
    40% {
      transform: translateY(40vh) translateX(15px) rotate(144deg) scale(1);
    }
    50% {
      transform: translateY(50vh) translateX(-30px) rotate(180deg) scale(0.9);
    }
    65% {
      transform: translateY(65vh) translateX(-10px) rotate(234deg) scale(1);
    }
    75% {
      transform: translateY(75vh) translateX(30px) rotate(270deg) scale(1.1);
    }
    90% {
      transform: translateY(90vh) translateX(20px) rotate(324deg) scale(1);
      opacity: 1;
    }
    100% {
      transform: translateY(100vh) translateX(0) rotate(360deg) scale(0.8);
      opacity: 0;
    }
  }

  @keyframes sway {
    0%,
    100% {
      transform: rotate(-5deg);
    }
    50% {
      transform: rotate(5deg);
    }
  }

  .animate-float {
    animation: float ease-in-out infinite;
  }

  /* Add a subtle sway to each petal */
  .animate-float > div {
    animation: sway 3s ease-in-out infinite;
    transform-origin: center;
  }

  .shadow-sakura {
    filter: drop-shadow(0 0 12px #ff79c6) drop-shadow(0 0 6px #fff2fa);
  }
</style>
