<script setup>
import NavItem from '@/components/NavItem.vue'
import { NAV_ITEMS } from '@/constants'

defineProps({
  currentPage: {
    type: String,
    required: true
  }
})

const emit = defineEmits(['navigate'])
</script>

<template>
  <nav class="sticky bottom-0 z-10 bg-white">
    <ul class="flex items-center justify-around border-t">
      <NavItem
        v-for="(icon, page) in NAV_ITEMS"
        :key="page"
        :href="`#${page}`"
        :class="{ 'pointer-events-none bg-gray-200': page == currentPage }"
        @click="emit('navigate', page)"
      >
        <component :is="icon" class="h-7" />
        {{ page }}
      </NavItem>
    </ul>
  </nav>
</template>
