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
  <svg class="ui-sprite-icon">
    <use :xlink:href="`src/shared/assets/vector/sprites/${spriteName}#${iconId}`" />
  </svg>
</template>

<style scoped>
@import "style.css";
</style>
