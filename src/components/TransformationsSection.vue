<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Autoplay } from 'swiper/modules'
import 'swiper/css'
import { ref, onMounted } from 'vue'

const fatLoss = ref(0)

onMounted(() => {
  let i = 0
  const interval = setInterval(() => {
    if (i < 18) {
      i++
      fatLoss.value = i
    } else {
      clearInterval(interval)
    }
  }, 60)
})
</script>

<template>
  <section
    id="transformations"
    class="relative overflow-hidden bg-black text-white py-32"
    style="will-change: transform;"
  >

    <!-- BACKGROUND GLOW -->
    <div class="absolute inset-0 overflow-hidden">

      <div
        class="absolute top-[-200px] left-[-150px]
              w-[500px] h-[500px]
              bg-lime-500/10 blur-[160px] rounded-full
              animate-pulse"
      ></div>

      <div
        class="absolute bottom-[-200px] right-[-150px]
              w-[600px] h-[600px]
              bg-cyan-500/10 blur-[180px] rounded-full
              animate-pulse"
      ></div>

    </div>

    <div class="container px-4 relative z-10">

      <!-- HEADER -->
      <div class="text-center mb-20">

        <p class="text-lime-400 tracking-[0.4em] uppercase mb-3">
          Real Results
        </p>

        <h2 class="text-4xl md:text-6xl font-black">
          Transformations That Inspire
        </h2>

        <p class="text-gray-400 mt-5 max-w-2xl mx-auto">
          See how our members changed their bodies and lives through discipline and consistency.
        </p>

      </div>

      <!-- GRID -->
      <div class="grid lg:grid-cols-2 gap-12 items-center">

        <!-- LEFT SIDE (BEFORE/AFTER) -->
        <div class="relative">

          <!-- SWIPER -->
          <Swiper
            :slides-per-view="1"
            :space-between="20"
            :grab-cursor="true"
            :loop="true"
            :autoplay="{
              delay: 1800,
              pauseOnMouseEnter: true,
              disableOnInteraction: false
            }"
            :modules="[Autoplay]"
            class="rounded-3xl overflow-hidden border border-white/10"
          >

            <SwiperSlide>
              <div class="relative">
                <img
                  src="https://images.unsplash.com/photo-1599058917212-d750089bc07e"
                  class="w-full h-[450px] object-cover"
                />
                <div class="absolute top-4 left-4 bg-black/70 px-4 py-2 rounded-full text-sm">
                  BEFORE
                </div>
              </div>
            </SwiperSlide>

            <SwiperSlide>
              <div class="relative">
                <img
                  src="https://images.unsplash.com/photo-1583454110551-21f2fa2afe61"
                  class="w-full h-[450px] object-cover"
                />
                <div class="absolute top-4 left-4 bg-lime-400 text-black px-4 py-2 rounded-full text-sm font-bold">
                  AFTER
                </div>
              </div>
            </SwiperSlide>

          </Swiper>

          <!-- PROGRESS BADGE (FUERA DEL SWIPER) -->
          <div
            class="absolute -bottom-6 right-6
                  bg-white/5 backdrop-blur-xl
                  border border-white/10 rounded-2xl
                  px-6 py-4 shadow-2xl z-10"
          >
            <p class="text-gray-400 text-sm">Body Fat Reduction</p>

            <h3 class="text-2xl font-black text-lime-400">
              -{{ fatLoss }}%
            </h3>
          </div>

        </div>

        <!-- RIGHT SIDE (TESTIMONIALS) -->
        <div class="space-y-8">

          <!-- CARD 1 -->
          <div
            class="bg-white/5 border border-white/10 rounded-3xl p-8 backdrop-blur-xl"
          >
            <p class="text-gray-300 mb-6">
              “This program completely changed my life. I lost 12kg in 3 months and feel stronger than ever.”
            </p>

            <div class="flex items-center gap-4">
              <img
                src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e"
                class="w-12 h-12 rounded-full object-cover"
              />

              <div>
                <h4 class="font-bold">Michael R.</h4>
                <p class="text-gray-400 text-sm">Member for 6 months</p>
              </div>
            </div>
          </div>

          <!-- CARD 2 -->
          <div
            class="bg-white/5 border border-white/10 rounded-3xl p-8 backdrop-blur-xl"
          >
            <p class="text-gray-300 mb-6">
              “The HIIT program gave me energy I never had before. I feel transformed mentally and physically.”
            </p>

            <div class="flex items-center gap-4">
              <img
                src="https://images.unsplash.com/photo-1544005313-94ddf0286df2"
                class="w-12 h-12 rounded-full object-cover"
              />

              <div>
                <h4 class="font-bold">Sarah L.</h4>
                <p class="text-gray-400 text-sm">Member for 4 months</p>
              </div>
            </div>
          </div>

          <!-- CARD 3 -->
          <div
            class="bg-white/5 border border-white/10 rounded-3xl p-8 backdrop-blur-xl"
          >
            <p class="text-gray-300 mb-6">
              “Best fitness decision I’ve ever made. The structure and coaching are next level.”
            </p>

            <div class="flex items-center gap-4">
              <img
                src="https://images.unsplash.com/photo-1552374196-c4e7ffc6e126"
                class="w-12 h-12 rounded-full object-cover"
              />

              <div>
                <h4 class="font-bold">David K.</h4>
                <p class="text-gray-400 text-sm">Member for 1 year</p>
              </div>
            </div>
          </div>

        </div>

      </div>

    </div>

  </section>
</template>