<template>
  <div class="min-h-screen bg-gray-100">
    <header class="bg-white shadow p-4 flex justify-between items-center">
      <h1 class="text-xl font-bold">Portfólio</h1>
      <nav class="space-x-4">
        <router-link to="/" class="text-blue-600 hover:underline">Home</router-link>
        <router-link to="/sobre" class="text-blue-600 hover:underline">Sobre</router-link>
        <router-link to="/contato" class="text-blue-600 hover:underline">Contato</router-link>
      </nav>
    </header>
    <main class="p-6">
      <router-view />
    </main>
  </div>
</template>
