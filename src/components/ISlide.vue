<script setup lang="ts">
import { ref, onMounted } from 'vue'

const show = ref(false)
onMounted(() => {
  show.value = true
})
</script>

<template>
  <div v-if="show" class="i-slide">
    <slot />
  </div>
</template>