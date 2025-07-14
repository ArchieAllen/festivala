<template>
  <header
    class="bg-gradient-to-r from-pink-500 via-purple-600 to-indigo-700 p-6 transition duration-700 ease-in-out flex items-center justify-between">
    <h1
      class="text-white text-3xl font-bold tracking-wider drop-shadow-md hover:scale-105 transition-transform duration-300">
      Archie's Festival
    </h1>

    <!-- Navigation Links -->
    <nav class="flex gap-6 text-white text-lg font-medium">
      <a href="home" class="hover:underline hover:text-yellow-300 transition duration-300 ease-in-out">Home</a>
      <a href="lineup" class="hover:underline hover:text-yellow-300 transition duration-300 ease-in-out">Lineup</a>
      <a href="ticket" class="hover:underline hover:text-yellow-300 transition duration-300 ease-in-out">Tickets</a>
      <a href="contact" class="hover:underline hover:text-yellow-300 transition duration-300 ease-in-out">Contact</a>
      <a href="merch" class="hover:underline hover:text-yellow-300 transiton duration-300 ease-in-out">Merch</a>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Navbar',
};
</script>

<style scoped>
/* Add a subtle pulse animation for extra flair */
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