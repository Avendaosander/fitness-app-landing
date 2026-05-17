<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Autoplay, Pagination } from 'swiper/modules'
import 'swiper/css'
import 'swiper/css/pagination'
import { ref, onMounted } from 'vue'

const fatLoss = ref(0)

const testimonials = [
  {
    quote:
      'This program completely changed my life. I lost 12kg in 3 months and feel stronger than ever.',
    name: 'Michael R.',
    role: 'Member for 6 months',
    image: 'https://images.unsplash.com/photo-1500648767791-00dcc994a43e',
  },
  {
    quote:
      'The HIIT program gave me energy I never had before. I feel transformed mentally and physically.',
    name: 'Sarah L.',
    role: 'Member for 4 months',
    image: 'https://images.unsplash.com/photo-1544005313-94ddf0286df2',
  },
  {
    quote:
      'Best fitness decision I’ve ever made. The structure and coaching are next level.',
    name: 'David K.',
    role: 'Member for 1 year',
    image: 'https://images.unsplash.com/photo-1552374196-c4e7ffc6e126',
  },
]

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
    class="relative overflow-hidden bg-black text-white py-16 sm:py-24 lg:py-32"
  >
    <div class="absolute inset-0 overflow-hidden pointer-events-none">
      <div
        class="absolute top-[-200px] left-[-150px]
              w-[280px] h-[280px] sm:w-[500px] sm:h-[500px]
              bg-lime-500/10 blur-[160px] rounded-full animate-pulse"
      ></div>
      <div
        class="absolute bottom-[-200px] right-[-150px]
              w-[320px] h-[320px] sm:w-[600px] sm:h-[600px]
              bg-cyan-500/10 blur-[180px] rounded-full animate-pulse"
      ></div>
    </div>

    <div class="max-w-7xl mx-auto w-full px-4 relative z-10">
      <div class="text-center mb-12 md:mb-20">
        <p class="text-lime-400 tracking-[0.2em] sm:tracking-[0.4em] uppercase mb-3 text-sm sm:text-base">
          Real Results
        </p>
        <h2 class="text-3xl sm:text-4xl md:text-6xl font-black px-2">
          Transformations That Inspire
        </h2>
        <p class="text-gray-400 mt-5 max-w-2xl mx-auto text-sm sm:text-base px-2">
          See how our members changed their bodies and lives through discipline and consistency.
        </p>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 lg:gap-12 items-start lg:items-center">
        <div class="relative w-full min-w-0">
          <Swiper
            :slides-per-view="1"
            :space-between="20"
            :grab-cursor="true"
            :loop="true"
            :autoplay="{
              delay: 1800,
              pauseOnMouseEnter: true,
              disableOnInteraction: false,
            }"
            :modules="[Autoplay]"
            class="w-full rounded-3xl overflow-hidden border border-white/10"
          >
            <SwiperSlide class="!w-full">
              <div class="relative w-full">
                <img
                  src="https://images.unsplash.com/photo-1599058917212-d750089bc07e"
                  alt="Before transformation"
                  class="w-full h-56 sm:h-72 md:h-96 lg:h-[450px] object-cover"
                />
                <div class="absolute top-4 left-4 bg-black/70 px-4 py-2 rounded-full text-sm">
                  BEFORE
                </div>
              </div>
            </SwiperSlide>

            <SwiperSlide class="!w-full">
              <div class="relative w-full">
                <img
                  src="https://images.unsplash.com/photo-1583454110551-21f2fa2afe61"
                  alt="After transformation"
                  class="w-full h-56 sm:h-72 md:h-96 lg:h-[450px] object-cover"
                />
                <div class="absolute top-4 left-4 bg-lime-400 text-black px-4 py-2 rounded-full text-sm font-bold">
                  AFTER
                </div>
              </div>
            </SwiperSlide>
          </Swiper>

          <div
            class="mt-4 mx-auto w-fit
                   min-[425px]:absolute min-[425px]:mx-0 min-[425px]:mt-0 min-[425px]:-bottom-6 min-[425px]:right-6
                   bg-white/5 backdrop-blur-xl border border-white/10
                   px-3 py-2 rounded-xl shadow-2xl z-10 text-center
                   min-[425px]:text-left
                   min-[550px]:px-5 min-[550px]:py-3 min-[550px]:rounded-2xl
                   sm:px-6 sm:py-4"
          >
            <div>
              <p class="text-gray-400 text-xs min-[550px]:text-sm">Body Fat Reduction</p>
              <h3 class="text-lg min-[550px]:text-xl sm:text-2xl font-black text-lime-400">-{{ fatLoss }}%</h3>
            </div>
          </div>
        </div>

        <div class="w-full min-w-0">
          <Swiper
            :slides-per-view="1"
            :space-between="16"
            :loop="true"
            :grab-cursor="true"
            :pagination="{ clickable: true }"
            :autoplay="{
              delay: 4000,
              pauseOnMouseEnter: true,
              disableOnInteraction: false,
            }"
            :modules="[Pagination, Autoplay]"
            class="testimonials-swiper w-full pb-10 lg:hidden"
          >
            <SwiperSlide
              v-for="testimonial in testimonials"
              :key="testimonial.name"
              class="!h-auto"
            >
              <div class="bg-white/5 border border-white/10 rounded-3xl p-6 sm:p-8 backdrop-blur-xl h-full">
                <p class="text-gray-300 mb-6 text-sm sm:text-base">“{{ testimonial.quote }}”</p>
                <div class="flex items-center gap-4">
                  <img
                    :src="testimonial.image"
                    :alt="testimonial.name"
                    class="w-12 h-12 rounded-full object-cover shrink-0"
                  />
                  <div class="min-w-0">
                    <h4 class="font-bold">{{ testimonial.name }}</h4>
                    <p class="text-gray-400 text-sm">{{ testimonial.role }}</p>
                  </div>
                </div>
              </div>
            </SwiperSlide>
          </Swiper>

          <div class="hidden lg:flex lg:flex-col lg:space-y-8">
            <div
              v-for="testimonial in testimonials"
              :key="`desktop-${testimonial.name}`"
              class="bg-white/5 border border-white/10 rounded-3xl p-8 backdrop-blur-xl"
            >
              <p class="text-gray-300 mb-6">“{{ testimonial.quote }}”</p>
              <div class="flex items-center gap-4">
                <img
                  :src="testimonial.image"
                  :alt="testimonial.name"
                  class="w-12 h-12 rounded-full object-cover shrink-0"
                />
                <div>
                  <h4 class="font-bold">{{ testimonial.name }}</h4>
                  <p class="text-gray-400 text-sm">{{ testimonial.role }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.testimonials-swiper :deep(.swiper-pagination-bullet) {
  background: rgba(255, 255, 255, 0.35);
  opacity: 1;
}

.testimonials-swiper :deep(.swiper-pagination-bullet-active) {
  background: #a3e635;
}
</style>
