<script setup>
import { CheckBadgeIcon } from '@heroicons/vue/24/solid'
</script>
<template>
  <a href="#" class="text-sm">
    <div v-if="false" class="flex items-center gap-2">
      <span>Day complete!</span>
      <CheckBadgeIcon class="h-7 text-green-500" />
    </div>
    <div v-else class="flex items-center gap-2">
      <div>Progress: <span class="font-mono">20%</span></div>
      <div class="h-3 w-3 rounded-full bg-red-500"></div>
    </div>
  </a>
</template>
