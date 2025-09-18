<script setup lang="ts">
import Navbar from './assets/componentes/Navbar.vue';
import QuickForm from './assets/componentes/QuickForm.vue';
import Sidebar from './assets/componentes/Sidebar.vue';
import StatsCards from './assets/componentes/StatsCards.vue';


</script>

<template>
  <div class="min-h-screen">
    <!-- Navbar -->
    <Navbar />

    <div class="flex">
      <!-- Sidebar -->
      <Sidebar />

      <!-- Main content -->
      <main class="flex-1 p-6">
        <div class="max-w-7xl mx-auto">
          <h2 class="text-2xl font-bold text-gray-800 mb-6">Panel de Control</h2>

          <!-- Stats -->
          <StatsCards />

          <div class="grid grid-cols-1 lg:grid-cols-2 gap-6">
            <!-- Formulario -->
            <QuickForm />

            <!-- Actividad reciente -->
            <div class="bg-white rounded-lg p-6 shadow-lg">
              <h3 class="text-lg font-semibold text-gray-800 mb-4">Actividad Reciente</h3>
              <div class="space-y-3">
                <div class="flex items-center justify-between p-3 bg-gray-100 rounded">
                  <span class="text-sm text-gray-600">Nuevo usuario registrado</span>
                  <span class="text-xs text-gray-500">Hace 2 min</span>
                </div>
                <div class="flex items-center justify-between p-3 bg-gray-100 rounded">
                  <span class="text-sm text-gray-600">Venta completada</span>
                  <span class="text-xs text-gray-500">Hace 5 min</span>
                </div>
                <div class="flex items-center justify-between p-3 bg-gray-100 rounded">
                  <span class="text-sm text-gray-600">Reporte generado</span>
                  <span class="text-xs text-gray-500">Hace 10 min</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </main>
    </div>
  </div>
</template>
