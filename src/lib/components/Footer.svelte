<script>
  // For copyright year
  const year = new Date().getFullYear();
</script>

<footer
  class="relative w-full py-8 px-4 flex flex-col items-center justify-center bg-slate-900/80 backdrop-blur-md border-t-2 border-pink-400/30 shadow-lg overflow-hidden"
>
  <!-- Neon animated border -->
  <div class="pointer-events-none absolute inset-0 z-0">
    <div
      class="absolute top-0 left-0 w-32 h-32 border-t-2 border-l-2 border-purple-400/40 animate-neon-glow"
    ></div>
    <div
      class="absolute bottom-0 right-0 w-32 h-32 border-b-2 border-r-2 border-pink-400/40 animate-neon-glow"
    ></div>
    <div
      class="absolute inset-0 rounded-xl border-2 border-pink-400/20 blur-[2px] animate-pulse-slow"
    ></div>
  </div>
  <!-- Footer content -->
  <div class="relative z-10 flex flex-col items-center gap-2">
    <div class="flex items-center gap-2">
      <span class="text-purple-300 text-sm">kimiz macOS Windows Gaming</span>
    </div>
    <div class="flex items-center gap-3 mt-2">
      <a
        href="https://github.com/kimiz-org/kimiz"
        target="_blank"
        rel="noopener"
        class="footer-icon-btn"
        aria-label="GitHub"
      >
        <i class="fa-brands fa-github"></i>
      </a>
      <a
        href="mailto:ahmet.affan.ebcioglu@outlook.com"
        class="footer-icon-btn"
        aria-label="Email"
      >
        <i class="fa-solid fa-envelope"></i>
      </a>
    </div>
    <div class="mt-2 text-xs text-gray-400">
      &copy; {year} kimiz.
    </div>
  </div>
</footer>

<style>
  .cyber-text-glow {
    text-shadow: 0 0 10px var(--primary);
  }
  .footer-icon-btn {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 2.75rem;
    height: 2.75rem;
    border-radius: 0.75rem;
    background: rgba(30, 27, 54, 0.7);
    border: 2px solid rgba(139, 233, 253, 0.25);
    color: #8be9fd;
    font-size: 1.5rem;
    box-shadow: 0 0 12px 0 rgba(139, 233, 253, 0.15);
    transition:
      border-color 0.2s,
      color 0.2s,
      box-shadow 0.2s,
      background 0.2s;
    overflow: hidden;
    z-index: 1;
  }
  .footer-icon-btn:hover,
  .footer-icon-btn:focus {
    border-color: #ff79c6;
    color: #ff79c6;
    background: linear-gradient(
      90deg,
      rgba(255, 121, 198, 0.12) 0%,
      rgba(189, 147, 249, 0.12) 100%
    );
    box-shadow:
      0 0 18px 0 #ff79c6,
      0 0 8px 0 #bd93f9;
    outline: none;
  }
  .footer-icon-btn:active {
    border-color: #bd93f9;
    color: #bd93f9;
    background: linear-gradient(
      90deg,
      rgba(189, 147, 249, 0.18) 0%,
      rgba(255, 121, 198, 0.18) 100%
    );
    box-shadow: 0 0 10px 0 #bd93f9;
  }
</style>
