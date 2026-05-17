<template>
  <footer class="relative bg-black text-white pt-24 pb-12 overflow-hidden">

    <!-- BACKGROUND GLOW -->
    <div class="absolute inset-0 pointer-events-none">
      <div class="absolute top-[-200px] left-[-200px] w-[500px] h-[500px] bg-lime-500/10 blur-[160px] rounded-full"></div>
      <div class="absolute bottom-[-200px] right-[-200px] w-[500px] h-[500px] bg-cyan-500/10 blur-[160px] rounded-full"></div>
    </div>

    <div class="container mx-auto px-6 relative z-10">

      <!-- TOP GRID -->
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-12 text-center sm:text-left mb-16">

        <!-- BRAND -->
        <div class="flex flex-col items-center sm:items-start">
          <h2 class="text-3xl font-black mb-4 tracking-tight">
            FIT<span class="text-lime-400">X</span>
          </h2>

          <p class="text-gray-400 text-sm leading-relaxed max-w-xs">
            Transform your body and mind with next-generation fitness training designed for real results.
          </p>
        </div>

        <!-- LINKS 1 -->
        <div>
          <h3 class="font-semibold mb-5 text-white/90">Product</h3>

          <ul class="space-y-3 text-gray-400 p-0">
            <li>
              <a href="#programs" class="hover:text-lime-400 no-underline transition">
                Programs
              </a>
            </li>
            <li>
              <a href="#pricing" class="hover:text-lime-400 no-underline transition">
                Pricing
              </a>
            </li>
            <li>
              <a href="#transformations" class="hover:text-lime-400 no-underline transition">
                Results
              </a>
            </li>
          </ul>
        </div>

        <!-- LINKS 2 -->
        <div>
          <h3 class="font-semibold mb-5 text-white/90">Company</h3>

          <ul class="space-y-3 text-gray-400 p-0">
            <li>
              <a href="#" class="hover:text-cyan-400 no-underline transition">
                About
              </a>
            </li>
            <li>
              <a href="#" class="hover:text-cyan-400 no-underline transition">
                Careers
              </a>
            </li>
            <li>
              <a href="#" class="hover:text-cyan-400 no-underline transition">
                Contact
              </a>
            </li>
          </ul>
        </div>

        <!-- SOCIAL -->
        <div class="flex flex-col items-center sm:items-start">
          <h3 class="font-semibold mb-5 text-white/90">Follow us</h3>

          <div class="flex flex-wrap justify-center sm:justify-start gap-4 text-sm text-gray-400">

            <a href="#" class="hover:text-lime-400 no-underline transition">
              Instagram
            </a>

            <a href="#" class="hover:text-cyan-400 no-underline transition">
              YouTube
            </a>

            <a href="#" class="hover:text-pink-400 no-underline transition">
              TikTok
            </a>

          </div>
        </div>

      </div>

      <!-- DIVIDER -->
      <div class="border-t border-white/10 pt-8 flex flex-col md:flex-row justify-between items-center gap-6 text-center">

        <p class="text-gray-500 text-sm">
          © 2026 FITX. All rights reserved.
        </p>

        <div class="flex flex-wrap justify-center gap-6 text-gray-500 text-sm">

          <a href="#" class="hover:text-white no-underline transition">
            Privacy Policy
          </a>

          <a href="#" class="hover:text-white no-underline transition">
            Terms of Service
          </a>

        </div>

      </div>

    </div>

  </footer>
</template>