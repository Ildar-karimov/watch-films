<script setup lang="ts">

</script>

<template>
<div class="page-sidebar">
  <nav class="page-sidebar__nav nav">
    <router-link
        to="/"
        class="nav__link"
    >
      Главная
    </router-link>
    <router-link
        to="/test3"
        class="nav__link"
    >
      Фильмы
    </router-link>
    <router-link
        to="/test2"
        class="nav__link"
    >
      Сериалы
    </router-link>
    <router-link
        to="/test"
        class="nav__link"
    >
      Мое
    </router-link>
  </nav>
</div>
</template>

<style lang="scss" scoped>
@use 'src/assets/scss/const/pallete/background-colors' as *;
@use 'src/assets/scss/const/pallete/font-colors' as *;

.page-sidebar {
  width: 220px;
  height: 100vh;
  padding: 15px 0;

  background-color: map-get($backgroundColors, primary);
}

.nav {
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 4px 0;

  .nav__link {
    padding: 10px 30px;

    color: map-get($fontColors, primary);

    &:hover, &.router-link-active {
      color: map-get($fontColors, primary-hover);

      background-color: map-get($backgroundColors, primary-hover);
    }
  }
}
</style>