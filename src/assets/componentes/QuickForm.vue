<script setup lang="ts">
import { ref } from "vue"

const formData = ref({
  nombre: "",
  email: "",
  password: "",
  confirmPassword: "",
})

const isSubmitted = ref(false)

const handleSubmit = () => {
  console.log("Form submitted:", formData.value)
  isSubmitted.value = true
}
</script>

<template>
  <div class="shadow-lg rounded-lg border border-gray-200 bg-white">
    <!-- Header -->
    <div class="px-4 py-3">
      <h2 class="text-gray-700 font-semibold">Registro Rápido</h2>
    </div>

    <!-- Content -->
    <div class="p-4">
      <form @submit.prevent="handleSubmit" class="grid grid-cols-2 gap-4">
        <!-- Nombre -->
        <div class="space-y-2">
          <label for="nombre" class="block text-sm font-medium">Nombre</label>
          <input
            id="nombre"
            v-model="formData.nombre"
            type="text"
            placeholder="Ingresa tu nombre"
            class="border rounded px-4 py-2 w-full focus:ring-2 focus:ring-indigo-500"
          />
        </div>

        <!-- Email -->
        <div class="space-y-2">
          <label for="email" class="block text-sm font-medium">Email</label>
          <input
            id="email"
            v-model="formData.email"
            type="email"
            placeholder="tu@email.com"
            class="border rounded px-4 py-2 w-full focus:ring-3 focus:ring-indigo-500"
          />
        </div>

        <!-- Password -->
        <div class="space-y-2">
          <label for="password" class="block text-sm font-medium">Contraseña</label>
          <input
            id="password"
            v-model="formData.password"
            type="password"
            placeholder="••••••••"
            class="border rounded px-4 py-2 w-full focus:ring-3 focus:ring-indigo-500"
          />
        </div>

        <!-- Confirm Password -->
        <div class="space-y-2">
          <label for="confirmPassword" class="block text-sm font-medium">Confirmar Contraseña</label>
          <input
            id="confirmPassword"
            v-model="formData.confirmPassword"
            type="password"
            placeholder="••••••••"
            class="border rounded px-4 py-2 w-full focus:ring-2 focus:ring-indigo-500"
          />
        </div>

        <!-- Submit -->
        <div class="col-span-2">
          <button
            type="submit"
            :class="[
              'px-6 py-2 rounded transition w-full',
              isSubmitted
                ? 'bg-green-600 hover:bg-green-700 text-white'
                : 'bg-indigo-600 hover:bg-indigo-700 text-white'
            ]"
          >
            {{ isSubmitted ? "Completado ✅" : "Registrar Usuario" }}
          </button>
        </div>
      </form>
    </div>
  </div>
</template>
