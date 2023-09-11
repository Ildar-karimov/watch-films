<script setup lang="ts">
import SpriteIcon from '@/components/ui/SpriteIcon.vue'

const spriteName: string = 'sidebar-sprite.svg'
</script>

<template>
  <div class="page-sidebar">
    <nav class="page-sidebar__nav nav">
      <router-link to="/" class="nav__link">
        <SpriteIcon :sprite-name="spriteName" icon-id="home" />
        Главная
      </router-link>
      <router-link to="/test3" class="nav__link">
        <SpriteIcon :sprite-name="spriteName" icon-id="film" />
        Фильмы
      </router-link>
      <router-link to="/test2" class="nav__link">
        <SpriteIcon :sprite-name="spriteName" icon-id="card" />
        Сериалы
      </router-link>
      <router-link to="/test" class="nav__link">
        <SpriteIcon sprite-name="sidebar-sprite.svg" icon-id="favorite-none" />
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
    display: flex;
    align-items: center;
    gap: 0 15px;
    padding: 10px 30px;

    color: map-get($fontColors, primary);

    &::v-deep(.sprite-icon) {
      fill: map-get($fontColors, primary);
    }

    &:hover,
    &.router-link-active {
      color: map-get($fontColors, primary-hover);

      background-color: map-get($backgroundColors, primary-hover);

      &::v-deep(.sprite-icon) {
        fill: map-get($fontColors, primary-hover);
      }
    }
  }
}
</style>
