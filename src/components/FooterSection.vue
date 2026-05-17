<template>
  <footer class="relative bg-black text-white pt-24 pb-12 overflow-hidden">

    <!-- BACKGROUND GLOW -->
    <div class="absolute inset-0">
      <div class="absolute top-[-200px] left-[-200px] w-[500px] h-[500px] bg-lime-500/10 blur-[160px] rounded-full"></div>
      <div class="absolute bottom-[-200px] right-[-200px] w-[500px] h-[500px] bg-cyan-500/10 blur-[160px] rounded-full"></div>
    </div>

    <div class="container px-4 relative z-10">

      <!-- TOP GRID -->
      <div class="grid md:grid-cols-4 gap-10 mb-16">

        <!-- BRAND -->
        <div>
          <h2 class="text-3xl font-black mb-4">
            FIT<span class="text-lime-400">X</span>
          </h2>

          <p class="text-gray-400 text-sm leading-relaxed">
            Transform your body and mind with next-generation fitness training.
          </p>
        </div>

        <!-- LINKS 1 -->
        <div>
          <h3 class="font-bold mb-4">Product</h3>
          <ul class="space-y-2 text-gray-400">
            <li><a href="#programs" class="hover:text-lime-400 transition">Programs</a></li>
            <li><a href="#pricing" class="hover:text-lime-400 transition">Pricing</a></li>
            <li><a href="#transformations" class="hover:text-lime-400 transition">Results</a></li>
          </ul>
        </div>

        <!-- LINKS 2 -->
        <div>
          <h3 class="font-bold mb-4">Company</h3>
          <ul class="space-y-2 text-gray-400">
            <li><a href="#" class="hover:text-lime-400 transition">About</a></li>
            <li><a href="#" class="hover:text-lime-400 transition">Careers</a></li>
            <li><a href="#" class="hover:text-lime-400 transition">Contact</a></li>
          </ul>
        </div>

        <!-- SOCIAL -->
        <div>
          <h3 class="font-bold mb-4">Follow us</h3>

          <div class="flex gap-4 text-gray-400">

            <a href="#" class="hover:text-lime-400 transition">Instagram</a>

            <a href="#" class="hover:text-cyan-400 transition">YouTube</a>

            <a href="#" class="hover:text-pink-400 transition">TikTok</a>

          </div>
        </div>

      </div>

      <!-- DIVIDER -->
      <div class="border-t border-white/10 pt-8 flex flex-col md:flex-row justify-between items-center gap-4">

        <p class="text-gray-500 text-sm">
          © 2026 FITX. All rights reserved.
        </p>

        <div class="flex gap-6 text-gray-500 text-sm">

          <a href="#" class="hover:text-white transition">Privacy Policy</a>
          <a href="#" class="hover:text-white transition">Terms of Service</a>

        </div>

      </div>

    </div>

  </footer>
</template>