<script setup lang="ts">
import { Home, Users, BarChart3 } from "lucide-vue-next"

const navItems = [
  { icon: Home, label: "Inicio", href: "#" },
  { icon: Users, label: "Usuarios", href: "#" },
  { icon: BarChart3, label: "Reportes", href: "#" },
]
</script>

<template>
  <aside class="hidden md:block w-64 h-screen bg-gray-100">
    <nav class="p-4">
      <ul class="space-y-2">
        <li v-for="(item, index) in navItems" :key="index">
          <a
            :href="item.href"
            class="flex items-center p-3 rounded-lg hover:bg-gray-200 transition-colors"
          >
            <!-- El icono dinámico -->
            <component
              :is="item.icon"
              class="h-5 w-5 mr-3 text-gray-600"
            />
            <span class="text-gray-700">{{ item.label }}</span>
          </a>
        </li>
      </ul>
    </nav>
  </aside>
</template>
