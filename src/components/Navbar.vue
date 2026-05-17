<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isScrolled = ref(false)
const isHidden = ref(false)
const activeSection = ref('home')

let lastScrollY = 0

const handleScroll = () => {
  const currentY = window.scrollY

  // blur navbar
  isScrolled.value = currentY > 40

  // hide/show navbar
  isHidden.value = currentY > lastScrollY && currentY > 200
  lastScrollY = currentY

  // scroll spy
  const sections = ['home', 'programs', 'transformations', 'pricing', 'contact']

  for (const id of sections) {
    const el = document.getElementById(id)
    if (!el) continue

    const rect = el.getBoundingClientRect()

    if (rect.top <= 120 && rect.bottom >= 120) {
      activeSection.value = id
    }
  }
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<template>

  <nav
    :class="[
      'fixed top-0 left-0 w-full z-50 transition-all duration-500',
      isScrolled
        ? 'bg-black/70 backdrop-blur-xl border-b border-white/10 py-4'
        : 'bg-transparent py-6',
      isHidden ? '-translate-y-full' : 'translate-y-0'
    ]"
  >

    <div class="container px-4">

      <div class="flex items-center justify-between">

        <!-- LOGO -->
        <a
          href="#home"
          class="text-2xl md:text-3xl font-black tracking-[0.25em]
                 text-white no-underline"
        >

          FIT<span class="text-lime-400">X</span>

        </a>

        <!-- DESKTOP MENU -->
        <div
          class="hidden lg:flex items-center gap-10"
        >

          <a
            href="#home"
            :class="[
              'relative text-gray-300 transition no-underline',
              activeSection === 'home'
                ? 'text-lime-400 drop-shadow-[0_0_8px_rgba(132,255,0,0.8)]'
                : 'hover:text-lime-400'
            ]"
          >
            Home

            <!-- underline animada -->
            <span
              class="absolute left-0 -bottom-1 h-[2px] bg-lime-400 transition-all duration-300"
              :class="activeSection === 'home' ? 'w-full' : 'w-0'"
            ></span>
          </a>

          <a
            href="#programs"
            :class="[
              'relative text-gray-300 transition no-underline',
              activeSection === 'programs'
                ? 'text-lime-400 drop-shadow-[0_0_8px_rgba(132,255,0,0.8)]'
                : 'hover:text-lime-400'
            ]"
          >
            Programs

            <!-- underline animada -->
            <span
              class="absolute left-0 -bottom-1 h-[2px] bg-lime-400 transition-all duration-300"
              :class="activeSection === 'programs' ? 'w-full' : 'w-0'"
            ></span>
          </a>

          <a
            href="#transformations"
            :class="[
              'relative text-gray-300 transition no-underline',
              activeSection === 'transformations'
                ? 'text-lime-400 drop-shadow-[0_0_8px_rgba(132,255,0,0.8)]'
                : 'hover:text-lime-400'
            ]"
          >
            Transformations

            <!-- underline animada -->
            <span
              class="absolute left-0 -bottom-1 h-[2px] bg-lime-400 transition-all duration-300"
              :class="activeSection === 'transformations' ? 'w-full' : 'w-0'"
            ></span>
          </a>

          <a
            href="#pricing"
            :class="[
              'relative text-gray-300 transition no-underline',
              activeSection === 'pricing'
                ? 'text-lime-400 drop-shadow-[0_0_8px_rgba(132,255,0,0.8)]'
                : 'hover:text-lime-400'
            ]"
          >
            Pricing

            <!-- underline animada -->
            <span
              class="absolute left-0 -bottom-1 h-[2px] bg-lime-400 transition-all duration-300"
              :class="activeSection === 'pricing' ? 'w-full' : 'w-0'"
            ></span>
          </a>

          <a
            href="#contact"
            :class="[
              'relative text-gray-300 transition no-underline',
              activeSection === 'contact'
                ? 'text-lime-400 drop-shadow-[0_0_8px_rgba(132,255,0,0.8)]'
                : 'hover:text-lime-400'
            ]"
          >
            Contact

            <!-- underline animada -->
            <span
              class="absolute left-0 -bottom-1 h-[2px] bg-lime-400 transition-all duration-300"
              :class="activeSection === 'contact' ? 'w-full' : 'w-0'"
            ></span>
          </a>

        </div>

        <!-- CTA -->
        <div class="hidden lg:block">

          <button
            class="px-6 py-3 rounded-full
                  bg-lime-400 text-black font-bold
                  hover:bg-lime-300 hover:scale-105
                  hover:shadow-[0_0_20px_rgba(132,255,0,0.5)]
                  transition duration-300"
          >
            Join Now
          </button>

        </div>

        <!-- MOBILE BUTTON -->
        <button
          class="lg:hidden flex flex-col gap-1"
          data-bs-toggle="collapse"
          data-bs-target="#mobileMenu"
        >

          <span class="w-7 h-[2px] bg-white"></span>
          <span class="w-7 h-[2px] bg-white"></span>
          <span class="w-7 h-[2px] bg-white"></span>

        </button>

      </div>

      <!-- MOBILE MENU -->
      <div
        id="mobileMenu"
        class="collapse lg:hidden"
      >

        <div
          class="mt-6 flex flex-col gap-5
                 bg-white/5 backdrop-blur-xl
                 border border-white/10
                 rounded-3xl p-6"
        >

          <a
            href="#home"
            class="text-gray-300 hover:text-lime-400 no-underline transition"
          >
            Home
          </a>

          <a
            href="#programs"
            class="text-gray-300 hover:text-lime-400 no-underline transition"
          >
            Programs
          </a>

          <a
            href="#transformations"
            class="text-gray-300 hover:text-lime-400 no-underline transition"
          >
            Transformations
          </a>

          <a
            href="#pricing"
            class="text-gray-300 hover:text-lime-400 no-underline transition"
          >
            Pricing
          </a>

          <a
            href="#contact"
            class="text-gray-300 hover:text-lime-400 no-underline transition"
          >
            Contact
          </a>

          <button
            class="mt-2 px-6 py-3 rounded-full
                   bg-lime-400 text-black font-bold
                   hover:bg-lime-300 transition"
          >
            Join Now
          </button>

        </div>

      </div>

    </div>

  </nav>

</template>