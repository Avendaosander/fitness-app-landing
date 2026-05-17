<template>
  <section
    id="contact"
    class="relative py-32 bg-black text-white overflow-hidden"
  >

    
    <div class="absolute inset-0">

      <div class="absolute top-[-200px] left-[-200px] w-[600px] h-[600px] bg-lime-500/20 blur-[180px] rounded-full"></div>

      <div class="absolute bottom-[-200px] right-[-200px] w-[600px] h-[600px] bg-cyan-500/20 blur-[180px] rounded-full"></div>

    </div>

    
    <div class="container px-4 relative z-10">

      <div class="max-w-4xl mx-auto text-center">

        
        <h2 class="text-4xl md:text-6xl font-black leading-tight mb-8">
          Tu versión más fuerte
          <span class="bg-gradient-to-r from-lime-400 to-cyan-400 bg-clip-text text-transparent">
            comienza hoy
          </span>
        </h2>

        
        <p class="text-gray-400 text-lg md:text-xl mb-12 max-w-2xl mx-auto">
          Únete a miles de atletas que están transformando sus cuerpos y mentes con nuestro sistema de entrenamiento.
          Sin excusas. Solo resultados.
        </p>

        
        <div class="flex flex-col sm:flex-row justify-center gap-5">

          <button
            class="px-10 py-4 rounded-full bg-lime-400 text-black font-bold text-lg
                   hover:bg-lime-300 hover:scale-105
                   hover:shadow-[0_0_50px_rgba(132,255,0,0.4)]
                   transition duration-300"
          >
            Comienza Prueba Gratis
          </button>

          <button
            class="px-10 py-4 rounded-full border border-white/20
                   bg-white/5 backdrop-blur-xl
                   hover:bg-white hover:text-black
                   transition duration-300"
          >
            Ver Prueba
          </button>

        </div>

        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-10 mt-20">

          <div>
            <h3 class="text-4xl font-black text-lime-400 mb-2">50K+</h3>
            <p class="text-gray-400">Miembros Activos</p>
          </div>

          <div>
            <h3 class="text-4xl font-black text-cyan-400 mb-2">1M+</h3>
            <p class="text-gray-400">Entrenamientos Completados</p>
          </div>

          <div>
            <h3 class="text-4xl font-black text-white mb-2">4.9★</h3>
            <p class="text-gray-400">Puntuación de Usuarios</p>
          </div>

        </div>

      </div>

    </div>

  </section>
</template>