<template>
  <!-- Loading Screen -->
  <div v-if="isLoading"
    class="fixed inset-0 z-50 flex flex-col items-center justify-center bg-gradient-to-r from-purple-600 via-pink-500 to-orange-400 text-white font-bold animate-fade-in">
    
    <!-- Spinning Icon -->
    <div class="mb-4 text-6xl animate-bounce">🎪</div>

    <!-- Loading Title -->
    <h2 class="text-5xl tracking-tight animate-pulse">Archie's Festival</h2>

    <!-- Tagline -->
    <p class="mt-4 text-xl text-white/80 animate-fade-in">Taking it to the extreme</p>
  </div>

  <!-- Main Page Content -->
  <div v-else
    class="relative min-h-screen bg-gradient-to-tr from-orange-400 via-pink-500 to-purple-700 text-white font-sans overflow-hidden">
    
    <!-- Particle Background -->
    <canvas id="particles-js" class="absolute top-0 left-0 w-full h-full z-0 opacity-20"></canvas>

    <!-- Radial Glow -->
    <div
      class="absolute top-0 left-0 w-full h-full bg-[radial-gradient(ellipse_at_center,_var(--tw-gradient-stops))] from-yellow-400 via-transparent to-transparent opacity-20 animate-pulse z-0">
    </div>

    <!-- Main Content -->
    <div class="relative z-10 flex flex-col items-center justify-center min-h-screen text-center">
      <h1
        class="text-7xl font-black tracking-tight drop-shadow-2xl bg-clip-text text-transparent bg-gradient-to-r from-yellow-300 via-red-400 to-pink-500 animate-gradient-x">
        Archie's Festival
      </h1>

      <p class="mt-6 text-xl text-white/80 animate-fade-in">The ultimate Festival</p>

      <div class="mt-12 flex gap-4">
        <button
          class="px-8 py-3 text-lg font-semibold bg-white text-pink-600 rounded-full shadow-lg hover:scale-105 hover:shadow-xl transition-all">
          <NuxtLink to="/ticket">Tickets</NuxtLink>
        </button>
        <button
          class="px-8 py-3 text-lg font-semibold bg-transparent border-2 border-white rounded-full hover:bg-white hover:text-pink-600 transition-all">
          <NuxtLink to="/merch">Merch</NuxtLink>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isLoading: true
    };
  },
  mounted() {
    // Show loading screen for 3 seconds
    setTimeout(() => {
      this.isLoading = false;
    }, 3000);
  }
};
</script>

<style scoped>
/* Gradient animation */
@keyframes gradient-x {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}

.animate-gradient-x {
  background-size: 200% 200%;
  animation: gradient-x 4s ease infinite;
}

/* Fade-in effect */
@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-fade-in {
  animation: fadeIn 1.5s ease forwards;
}

/* Bounce effect */
@keyframes bounce {
  0%, 100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-10px);
  }
}

.animate-bounce {
  animation: bounce 1s ease infinite;
}

/* Pulse effect */
.animate-pulse {
  animation: pulse 2s infinite;
}
</style>