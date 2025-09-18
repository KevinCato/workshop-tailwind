<script setup lang="ts">
import { User } from "lucide-vue-next"
</script>

<template>
  <nav class="flex justify-between items-center p-4 bg-indigo-600 text-white">
    <h1 class="text-xl font-bold">Dashboard</h1>

    <!-- Botón equivalente al de shadcn (variant ghost, size sm) -->
    <button
      class="flex items-center px-3 py-2 text-sm rounded-md text-white hover:bg-indigo-700 transition"
    >
      <User class="h-4 w-4 mr-2" />
      Usuario
    </button>
  </nav>
</template>
