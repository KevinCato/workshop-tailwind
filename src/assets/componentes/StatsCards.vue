<script setup lang="ts">
import { Users, ShoppingCart, DollarSign } from "lucide-vue-next"

const stats = [
  {
    title: "Usuarios",
    value: "1,234",
    icon: Users,
    change: "+12%",
  },
  {
    title: "Ventas",
    value: "856",
    icon: ShoppingCart,
    change: "+8%",
  },
  {
    title: "Ingresos",
    value: "$45,678",
    icon: DollarSign,
    change: "+15%",
  },
]
</script>

<template>
  <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-8">
    <div
      v-for="(stat, index) in stats"
      :key="index"
      class="bg-white shadow-lg rounded-xl p-4"
    >
      <div class="flex flex-row items-center justify-between pb-2">
        <h3 class="text-sm font-medium text-gray-700">
          {{ stat.title }}
        </h3>
        <component :is="stat.icon" class="h-4 w-4 text-gray-400" />
      </div>
      <div>
        <div class="text-2xl font-bold text-gray-700">
          {{ stat.value }}
        </div>
        <p class="text-xs text-gray-500">
          <span class="text-green-600">{{ stat.change }}</span> desde el mes pasado
        </p>
      </div>
    </div>
  </div>
</template>
