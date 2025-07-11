<template>
  <nav class="bg-gradient-to-r from-red-400 to-red-700 bg-opacity-75 p-4 shadow-lg">
    <div class="container mx-auto flex flex-col md:flex-row items-center justify-between">
      <div class="flex items-center space-x-4">
        <NuxtImg src="/icon.png" height="50" class="rounded-full" />
        <span class="text-white text-xl font-bold">Archies Festival</span>
      </div>
      <div class="hidden md:flex items-center space-x-6">
        <a href="" class="text-gray-300 hover:text-white transition duration-300">Home</a>
      <a href="tickets" class="text-gray-300 hover:text-white transition duration-300">Tickets</a>
      </div>
      <button class="md:hidden text-white focus:outline-none" @click="toggleMenu">
        <Icon name="heroicons-outline:menu" size="24" />
      </button>
    </div>
    <div v-if="menuOpen" class="md:hidden mt-4 flex flex-col space-y-2">
      <a href="" class="text-gray-300 hover:text-white transition duration-300">Home</a>
      <a href="tickets" class="text-gray-300 hover:text-white transition duration-300">Tickets</a>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      menuOpen: false,
    };
  },
  methods: {
    toggleMenu() {
      this.menuOpen = !this.menuOpen;
    },
  },
};
</script>