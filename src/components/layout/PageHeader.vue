<script setup lang="ts">

</script>

<template>
<header class="page-header">
  <img
      src="src/assets/vector/logo-large.svg"
      alt="watch movies"
  >
</header>
</template>

<style lang="scss" scoped>
@use 'src/assets/scss/const/pallete/gray' as *;
.page-header {
  display: flex;
  align-items: center;
  height: 72px;
  padding: 0 72px;

  background-color: map-get($grayColors, 900);
}
</style>