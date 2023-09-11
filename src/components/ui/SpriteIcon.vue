<script setup lang="ts">
defineProps({
  iconId: {
    type: String,
    required: true,
  },
  spriteName: {
    type: String,
    required: true,
  }
})
</script>

<template>
  <svg class="sprite-icon">
    <use :xlink:href="`src/assets/vector/sprites/${spriteName}#${iconId}`" />
  </svg>
</template>

<style scoped></style>
