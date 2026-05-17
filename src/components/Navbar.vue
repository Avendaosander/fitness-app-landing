<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isScrolled = ref(false)
const isHidden = ref(false)
const isMobileMenuOpen = ref(false)
const activeSection = ref('home')

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value
}

const closeMobileMenu = () => {
  isMobileMenuOpen.value = false
}

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

const handleResize = () => {
  if (window.innerWidth >= 1024) {
    closeMobileMenu()
  }
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
  window.addEventListener('resize', handleResize)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
  window.removeEventListener('resize', handleResize)
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
          type="button"
          class="lg:hidden flex flex-col justify-center gap-1.5 p-2 -mr-2"
          :aria-expanded="isMobileMenuOpen"
          aria-controls="mobileMenu"
          aria-label="Abrir menú de navegación"
          @click="toggleMobileMenu"
        >

          <span
            class="w-7 h-[2px] bg-white transition-transform duration-300 origin-center"
            :class="isMobileMenuOpen ? 'translate-y-[5px] rotate-45' : ''"
          ></span>
          <span
            class="w-7 h-[2px] bg-white transition-opacity duration-300"
            :class="isMobileMenuOpen ? 'opacity-0' : ''"
          ></span>
          <span
            class="w-7 h-[2px] bg-white transition-transform duration-300 origin-center"
            :class="isMobileMenuOpen ? '-translate-y-[5px] -rotate-45' : ''"
          ></span>

        </button>

      </div>

      <!-- MOBILE MENU -->
      <div
        v-show="isMobileMenuOpen"
        id="mobileMenu"
        class="lg:hidden"
      >

        <div
          class="mt-6 flex flex-col gap-5
                 bg-white/5 backdrop-blur-xl
                 border border-white/10
                 rounded-3xl p-6"
        >

          <a
            href="#home"
            :class="[
              'no-underline transition',
              activeSection === 'home'
                ? 'text-lime-400'
                : 'text-gray-300 hover:text-lime-400'
            ]"
            @click="closeMobileMenu"
          >
            Home
          </a>

          <a
            href="#programs"
            :class="[
              'no-underline transition',
              activeSection === 'programs'
                ? 'text-lime-400'
                : 'text-gray-300 hover:text-lime-400'
            ]"
            @click="closeMobileMenu"
          >
            Programs
          </a>

          <a
            href="#transformations"
            :class="[
              'no-underline transition',
              activeSection === 'transformations'
                ? 'text-lime-400'
                : 'text-gray-300 hover:text-lime-400'
            ]"
            @click="closeMobileMenu"
          >
            Transformations
          </a>

          <a
            href="#pricing"
            :class="[
              'no-underline transition',
              activeSection === 'pricing'
                ? 'text-lime-400'
                : 'text-gray-300 hover:text-lime-400'
            ]"
            @click="closeMobileMenu"
          >
            Pricing
          </a>

          <a
            href="#contact"
            :class="[
              'no-underline transition',
              activeSection === 'contact'
                ? 'text-lime-400'
                : 'text-gray-300 hover:text-lime-400'
            ]"
            @click="closeMobileMenu"
          >
            Contact
          </a>

          <button
            type="button"
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