<script setup lang="ts">

</script>

<template>
<header class="page-header">
  <img
      src="src/assets/vector/logo-large.svg"
      alt="watch movies"
  >
  <input
      type="text"
      class="page-header__search"
      placeholder="Введите для поиска"
  >
  <div class="page-header__user-block">
    Войти
  </div>
</header>
</template>

<style lang="scss" scoped>
@use 'src/assets/scss/const/pallete/gray' as *;
@use 'src/assets/scss/const/pallete/font-colors' as *;

.page-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 72px;
  padding: 0 72px;

  color: map-get($fontColors, primary);

  background-color: map-get($grayColors, 900);
}
</style>