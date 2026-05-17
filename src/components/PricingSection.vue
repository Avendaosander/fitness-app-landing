<template>
  <section id="pricing" class="py-32 bg-black text-white relative overflow-hidden">

    
    <div class="absolute inset-0">
      <div class="absolute top-[-200px] left-[-150px] w-[500px] h-[500px] bg-lime-500/10 blur-[160px] rounded-full"></div>
      <div class="absolute bottom-[-200px] right-[-150px] w-[500px] h-[500px] bg-cyan-500/10 blur-[160px] rounded-full"></div>
    </div>

    <div class="container px-4 relative z-10">

      
      <div class="text-center mb-20">

        <p class="text-lime-400 tracking-[0.4em] uppercase mb-3">
          Planes de precios
        </p>

        <h2 class="text-4xl md:text-6xl font-black">
          Elige tu nivel
        </h2>

        <p class="text-gray-400 mt-5 max-w-2xl mx-auto">
          Comienza gratis y mejora a medida que creces. Diseñado para todos los niveles de fitness.
        </p>

      </div>

      
      <div class="grid lg:grid-cols-3 gap-10">

        
        <div
          class="group relative bg-white/5 border border-white/10
                 rounded-3xl p-10 backdrop-blur-xl
                 hover:scale-[1.03] hover:border-white/20
                 transition duration-300"
        >

          <h3 class="text-2xl font-bold mb-2">Básico</h3>

          <p class="text-gray-400 mb-6">
            Comienza tu viaje fitness
          </p>

          <div class="text-5xl font-black mb-6">
            $0
            <span class="text-lg text-gray-400">/mes</span>
          </div>

          <ul class="space-y-3 text-gray-300 mb-10">
            <li>✔ Acceso a ejercicios</li>
            <li>✔ Seguimiento básico</li>
            <li>✔ Acceso a la comunidad</li>
          </ul>

          <button
            class="w-full py-3 rounded-full border border-white/20
                   hover:bg-white hover:text-black transition"
          >
            Comienza Gratis
          </button>

        </div>

        
        <div
          class="relative group bg-gradient-to-br from-lime-500/10 to-cyan-500/10
                 border border-lime-400/40
                 rounded-3xl p-10 backdrop-blur-xl
                 scale-105 shadow-[0_0_80px_rgba(132,255,0,0.15)]
                 hover:scale-[1.08] transition duration-300"
        >

          
          <div class="absolute top-6 right-6 bg-lime-400 text-black px-3 py-1 rounded-full text-xs font-bold">
            MÁS POPULAR
          </div>

          <h3 class="text-2xl font-bold mb-2">Pro</h3>

          <p class="text-gray-400 mb-6">
            Para deportistas serios
          </p>

          <div class="text-5xl font-black mb-6">
            $19
            <span class="text-lg text-gray-400">/mes</span>
          </div>

          <ul class="space-y-3 text-gray-300 mb-10">
            <li>✔ Todo en Básico</li>
            <li>✔ Planes personalizados</li>
            <li>✔ Seguimiento de progreso con IA</li>
            <li>✔ Guía de nutrición</li>
          </ul>

          <button
            class="w-full py-3 rounded-full bg-lime-400 text-black font-bold
                   hover:bg-lime-300 hover:shadow-[0_0_35px_rgba(132,255,0,0.5)]
                   transition"
          >
            Comienza Pro
          </button>

        </div>

        
        <div
          class="group relative bg-white/5 border border-white/10
                 rounded-3xl p-10 backdrop-blur-xl
                 hover:scale-[1.03] hover:border-white/20
                 transition duration-300"
        >

          <h3 class="text-2xl font-bold mb-2">Elite</h3>

          <p class="text-gray-400 mb-6">
            Modo de transformación completa
          </p>

          <div class="text-5xl font-black mb-6">
            $39
            <span class="text-lg text-gray-400">/mes</span>
          </div>

          <ul class="space-y-3 text-gray-300 mb-10">
            <li>✔ Todo en Pro</li>
            <li>✔ Coaching 1-on-1</li>
            <li>✔ Análisis avanzado</li>
            <li>✔ Soporte prioritario</li>
          </ul>

          <button
            class="w-full py-3 rounded-full border border-cyan-400
                   text-cyan-400 hover:bg-cyan-400 hover:text-black
                   transition"
          >
            Comienza Elite
          </button>

        </div>

      </div>

    </div>

  </section>
</template>