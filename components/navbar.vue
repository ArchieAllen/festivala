<template>
  <header
    class="bg-gradient-to-r from-pink-500 via-purple-600 to-indigo-700 p-6 transition duration-700 ease-in-out flex items-center justify-between">
    <h1
      class="text-white text-3xl font-bold tracking-wider drop-shadow-md hover:scale-105 transition-transform duration-300">
      Archie's Festival
    </h1>
    <nav class="flex gap-6 text-white text-lg font-medium">
      <a class="hover:underline hover:text-yellow-300 transition duration-300 ease-in-out">
        <NuxtLink to="/">Home</NuxtLink>
      </a>
      <a class="hover:underline hover:text-yellow-300 transition duration-300 ease-in-out">
        <NuxtLink to="/ticket">Tickets</NuxtLink>
      </a>
      <a class="hover:underline hover:text-yellow-300 transition duration-300 ease-in-out">
        <NuxtLink to="/contact">Contact</NuxtLink>
      </a>
      <a class="hover:underline hover:text-yellow-300 transition duration-300 ease-in-out">
        <NuxtLink to="/merch">Merch</NuxtLink>
      </a>
    </nav>
  </header>
</template>

<style scoped>
@keyframes pulseGlow {
  0% {
    box-shadow: 0 0 0px rgba(255, 255, 255, 0.4);
  }

  50% {
    box-shadow: 0 0 20px rgba(255, 255, 255, 0.6);
  }

  100% {
    box-shadow: 0 0 0px rgba(255, 255, 255, 0.4);
  }
}

header:hover {
  animation: pulseGlow 2s infinite;
}
</style>