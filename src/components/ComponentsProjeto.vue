<template>
  <div class="bg-white rounded-lg shadow-md p-6 hover:shadow-lg transition-shadow duration-300">
    <div class="flex items-center justify-between mb-4">
      <h3 class="text-xl font-semibold text-gray-800">{{ project.title }}</h3>
      <span class="px-3 py-1 bg-blue-100 text-blue-800 text-sm rounded-full">{{ project.status }}</span>
    </div>
    
    <p class="text-gray-600 mb-4">{{ project.description }}</p>
    
    <div class="mb-4">
      <h4 class="text-sm font-medium text-gray-700 mb-2">Tecnologias:</h4>
      <div class="flex flex-wrap gap-2">
        <span 
          v-for="tech in project.technologies" 
          :key="tech"
          class="px-2 py-1 bg-gray-100 text-gray-700 text-xs rounded"
        >
          {{ tech }}
        </span>
      </div>
    </div>
    
    <div class="flex gap-3">
      <a 
        v-if="project.githubUrl" 
        :href="project.githubUrl" 
        target="_blank"
        class="flex items-center gap-1 text-blue-600 hover:text-blue-800 text-sm"
      >
        🔗 GitHub
      </a>
    </div>
  </div>
</template>

<script setup>
defineProps({
  project: {
    type: Object,
    required: true
  }
})
</script>
