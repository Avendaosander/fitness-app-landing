<script setup>
import Fitness from '../assets/Male-Fitness.avif'
</script>

<template>
  <section
    id="home"
    class="relative min-h-screen overflow-hidden bg-black text-white flex items-center"
  >

    <!-- BACKGROUND GLOW -->
    <div
      class="absolute inset-0 overflow-hidden"
    >

      <!-- GREEN GLOW -->
      <div
        class="absolute top-[-200px] left-[-100px] w-[500px] h-[500px]
               bg-lime-500/20 blur-[140px] rounded-full"
      ></div>

      <!-- BLUE GLOW -->
      <div
        class="absolute bottom-[-200px] right-[-100px] w-[500px] h-[500px]
               bg-cyan-500/20 blur-[140px] rounded-full"
      ></div>

      <!-- GRID -->
      <div
        class="absolute inset-0 opacity-10"
        style="
          background-image:
          linear-gradient(rgba(255,255,255,0.08) 1px, transparent 1px),
          linear-gradient(90deg, rgba(255,255,255,0.08) 1px, transparent 1px);
          background-size: 60px 60px;
        "
      ></div>

    </div>

    <!-- CONTENT -->
    <div
      class="container relative z-10 flex items-center min-h-screen px-4"
    >

      <div
        class="grid lg:grid-cols-2 gap-16 items-center w-full py-20"
      >

        <!-- LEFT SIDE -->
        <div>

          <!-- BADGE -->
          <div
            class="inline-flex items-center gap-2 px-4 py-2 rounded-full
                   bg-white/5 border border-white/10 backdrop-blur-xl mb-8"
          >

            <div class="w-2 h-2 bg-lime-400 rounded-full animate-pulse"></div>

            <span class="text-sm tracking-widest text-gray-300">
              #1 FITNESS PLATFORM
            </span>

          </div>

          <!-- TITLE -->
          <h1
            class="text-5xl md:text-7xl lg:text-8xl font-black leading-[0.95] mb-8"
          >
            Transform
            <span
              class="bg-gradient-to-r from-lime-400 to-cyan-400 bg-clip-text text-transparent"
            >
              Your Body
            </span>

            <br />

            Elevate
            <br />
            Your Mind
          </h1>

          <!-- DESCRIPTION -->
          <p
            class="text-gray-400 text-lg md:text-xl leading-relaxed max-w-2xl mb-10"
          >
            Unlock your full potential with personalized workouts,
            elite coaching and next-generation fitness tracking.
          </p>

          <!-- BUTTONS -->
          <div
            class="flex flex-col sm:flex-row gap-4 mb-14"
          >

            <!-- PRIMARY -->
            <button
              class="px-8 py-4 rounded-full bg-lime-400 text-black font-bold
                     hover:scale-105 hover:bg-lime-300 transition duration-300
                     shadow-[0_0_40px_rgba(132,255,0,0.35)]"
            >
              Start Training
            </button>

            <!-- SECONDARY -->
            <button
              class="px-8 py-4 rounded-full border border-white/20
                     bg-white/5 backdrop-blur-xl
                     hover:bg-white hover:!text-black
                     transition duration-300"
            >
              Explore Programs
            </button>

          </div>

          <!-- STATS -->
          <div
            class="grid grid-cols-3 gap-6"
          >

            <div>
              <h3
                class="text-3xl md:text-4xl font-black text-lime-400 mb-2"
              >
                25K+
              </h3>

              <p class="text-gray-400 text-sm">
                Active Members
              </p>
            </div>

            <div>
              <h3
                class="text-3xl md:text-4xl font-black text-cyan-400 mb-2"
              >
                150+
              </h3>

              <p class="text-gray-400 text-sm">
                Elite Trainers
              </p>
            </div>

            <div>
              <h3
                class="text-3xl md:text-4xl font-black text-white mb-2"
              >
                98%
              </h3>

              <p class="text-gray-400 text-sm">
                Success Rate
              </p>
            </div>

          </div>

        </div>

        <!-- RIGHT SIDE -->
        <div
          class="relative flex items-center justify-center min-h-[650px]"
        >

          <!-- MAIN GLOW -->
          <div
            class="absolute w-[350px] md:w-[450px] h-[350px] md:h-[450px]
                  bg-gradient-to-r from-lime-400/20 to-cyan-400/20
                  rounded-full blur-[100px]"
          ></div>

          <!-- SECONDARY GLOW -->
          <div
            class="absolute bottom-10 w-[250px] h-[250px]
                  bg-lime-400/20 rounded-full blur-[120px]"
          ></div>

          <!-- IMAGE WRAPPER -->
          <div
            class="relative z-10 flex justify-center"
          >

            <img
              :src="Fitness"
              alt="Fitness Athlete"
              class="w-full max-w-[420px] md:max-w-[500px]
                    h-auto object-contain
                    drop-shadow-[0_20px_80px_rgba(0,0,0,0.8)]
                    animate-[float_5s_ease-in-out_infinite]"
            />

          </div>

          <!-- FLOATING CARD LEFT -->
          <div
            class="absolute top-20 left-2 md:left-10
                  bg-white/5 backdrop-blur-xl
                  border border-white/10
                  rounded-3xl px-5 py-4
                  shadow-2xl z-20"
          >

            <p class="text-gray-400 text-sm mb-1">
              Calories Burned
            </p>

            <h4 class="text-2xl md:text-3xl font-black text-lime-400">
              1,240
            </h4>

          </div>

          <!-- FLOATING CARD RIGHT -->
          <div
            class="absolute bottom-20 right-2 md:right-10
                  bg-white/5 backdrop-blur-xl
                  border border-white/10
                  rounded-3xl px-5 py-4
                  shadow-2xl z-20"
          >

            <p class="text-gray-400 text-sm mb-1">
              Weekly Progress
            </p>

            <h4 class="text-2xl md:text-3xl font-black text-cyan-400">
              +18%
            </h4>

          </div>

        </div>

      </div>

    </div>

  </section>
</template>