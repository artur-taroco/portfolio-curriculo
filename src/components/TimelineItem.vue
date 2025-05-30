<template>
  <div class="flex items-start space-x-4 mb-8">
    <div class="flex flex-col items-center">
      <div class="w-4 h-4 bg-blue-600 rounded-full border-4 border-white shadow"></div>
      <div v-if="!isLast" class="w-0.5 h-16 bg-gray-300 mt-2"></div>
    </div>
    
    <div class="flex-1 bg-white rounded-lg shadow-sm p-4 border-l-4 border-blue-600">
      <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between mb-2">
        <h3 class="text-lg font-semibold text-gray-800">{{ item.title }}</h3>
        <span class="text-sm text-gray-500 mt-1 sm:mt-0">{{ item.period }}</span>
      </div>
      
      <p class="text-blue-600 font-medium mb-2">{{ item.institution }}</p>
      <p class="text-gray-600 text-sm">{{ item.description }}</p>
      
      <div v-if="item.achievements && item.achievements.length" class="mt-3">
        <h4 class="text-sm font-medium text-gray-700 mb-1">Conquistas:</h4>
        <ul class="list-disc list-inside text-sm text-gray-600 space-y-1">
          <li v-for="achievement in item.achievements" :key="achievement">
            {{ achievement }}
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  item: {
    type: Object,
    required: true
  },
  isLast: {
    type: Boolean,
    default: false
  }
})
</script>
