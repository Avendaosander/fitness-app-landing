<script setup>
import { Flame, Dumbbell, Heart } from 'lucide-vue-next'
</script>

<template>
  <section id="programs" class="py-32 bg-black text-white">

    <div class="container px-4">

      
      <div class="text-center mb-20">

        <p class="text-lime-400 tracking-[0.4em] uppercase mb-3">
          Programas de Entrenamiento
        </p>

        <h2 class="text-4xl md:text-6xl font-black">
          Elige tu Camino
        </h2>

        <p class="text-gray-400 mt-5 max-w-2xl mx-auto">
          Ya sea que quieras construir fuerza, perder peso o mejorar tu resistencia,
          tenemos el programa perfecto para ti.
        </p>

      </div>

      
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-10">

        
        <div
          class="group relative bg-white/5 border border-white/10
                 rounded-3xl p-8 backdrop-blur-xl cursor-pointer
                 hover:border-white/20 hover:scale-[1.04] hover:shadow-[0_0_50px_rgba(132,255,0,0.08)] hover:-translate-y-2
                 transition duration-300"
        >

          <div class="text-lime-400 text-3xl mb-5">
            <Dumbbell class="w-10 h-10 text-lime-400 mb-5" />
          </div>

          <h3 class="text-2xl font-bold mb-3">
            Entrenamiento de Fuerza
          </h3>

          <p class="text-gray-400 mb-6">
            Construye masa muscular y aumenta tu fuerza con programas de sobrecarga progresiva.
          </p>

          <div class="text-sm text-gray-500 mb-6">
            8 Semanas • Avanzado • Basado en Gimnasio
          </div>

          <button
            class="w-full py-3 rounded-full bg-lime-400 text-black font-bold
                   hover:bg-lime-300 hover:shadow-[0_0_25px_rgba(132,255,0,0.4)]
                   transition"
          >
            Comienza el Programa
          </button>

          
          <div
            class="absolute inset-0 rounded-3xl opacity-0 group-hover:opacity-100
                   bg-lime-400/10 blur-2xl transition"
          ></div>

        </div>

        
        <div
          class="group relative bg-gradient-to-br from-cyan-500/10 to-white/5
                border border-cyan-400/40
                rounded-3xl p-8 backdrop-blur-xl cursor-pointer
                hover:border-white/20 hover:scale-[1.04] hover:shadow-[0_0_50px_rgba(132,255,0,0.08)] hover:-translate-y-2 transition duration-300
                shadow-[0_0_40px_rgba(34,211,238,0.15)]"
        >

          
          <div class="absolute top-5 right-5 text-xs px-3 py-1 rounded-full
                      bg-cyan-400 text-black font-bold">
            MÁS POPULAR
          </div>

          
          <Flame class="w-10 h-10 text-cyan-400 mb-5" />

          <h3 class="text-2xl font-bold mb-3">
            Entrenamiento HIIT
          </h3>

          <p class="text-gray-400 mb-6">
            Entrenamientos de alta intensidad diseñados para quemar calorías rápidamente y mejorar la condición física.
          </p>

          <div class="text-sm text-gray-500 mb-6">
            6 Semanas • Intermedio • Amigable para Casa
          </div>

          <button
            class="w-full py-3 rounded-full bg-cyan-400 text-black font-bold
                  hover:bg-cyan-300 hover:shadow-[0_0_35px_rgba(34,211,238,0.5)]
                  transition"
          >
            Comienza el Programa
          </button>

          
          <div
            class="absolute inset-0 rounded-3xl opacity-0 group-hover:opacity-100
                  bg-cyan-400/10 blur-2xl transition"
          ></div>

        </div>

        
        <div
          class="group relative bg-white/5 border border-white/10
                 rounded-3xl p-8 backdrop-blur-xl cursor-pointer
                 hover:border-white/20 hover:scale-[1.04] hover:shadow-[0_0_50px_rgba(132,255,0,0.08)] hover:-translate-y-2
                 transition duration-300"
        >

          <div class="text-pink-400 text-3xl mb-5">
            <Heart class="w-10 h-10 text-pink-400 mb-5" />
          </div>

          <h3 class="text-2xl font-bold mb-3">
            Mobilidad y Yoga
          </h3>

          <p class="text-gray-400 mb-6">
            Mejora tu flexibilidad, postura y reduce el riesgo de lesiones con sesiones guiadas.
          </p>

          <div class="text-sm text-gray-500 mb-6">
            4 Semanas • Principiante • Enfoque en Recuperación
          </div>

          <button
            class="w-full py-3 rounded-full bg-pink-400 text-black font-bold
                   hover:bg-pink-300 hover:shadow-[0_0_25px_rgba(236,72,153,0.4)]
                   transition"
          >
            Comienza el Programa
          </button>

          <div
            class="absolute inset-0 rounded-3xl opacity-0 group-hover:opacity-100
                   bg-pink-400/10 blur-2xl transition"
          ></div>

        </div>

      </div>

    </div>

  </section>
</template>