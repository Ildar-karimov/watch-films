<template>
  <aside class="page-sidebar">
    <nav class="page-sidebar__nav nav">
      <router-link to="/" class="nav__link">
        <UiSpriteIcon :sprite-name="SPRITE_NAME" icon-id="home" />
        Главная
      </router-link>
      <router-link to="/test3" class="nav__link">
        <UiSpriteIcon :sprite-name="SPRITE_NAME" icon-id="film" />
        Фильмы
      </router-link>
      <router-link to="/test2" class="nav__link">
        <UiSpriteIcon :sprite-name="SPRITE_NAME" icon-id="card" />
        Сериалы
      </router-link>
      <router-link to="/test" class="nav__link">
        <UiSpriteIcon sprite-name="sidebar-sprite.svg" icon-id="favorite-none" />
        Мое
      </router-link>
    </nav>
  </aside>
</template>

<script setup lang="ts">
import { UiSpriteIcon } from '@/shared/ui/UiSpriteIcon';

const SPRITE_NAME = 'sidebar-sprite.svg';
</script>


<style lang="scss" scoped>
@use '@/shared/assets/scss/consts/pallete/background-colors.scss' as *;
@use '@/shared/assets/scss/consts/pallete/font-colors.scss' as *;
@use '@/shared/assets/scss/consts/layoutVariables.scss' as *;

.page-sidebar {
  position: fixed;
  left: 0;
  top: $headerHeight;

  width: $sideBarWidth;
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

    &::v-deep(.ui-sprite-icon) {
      fill: map-get($fontColors, primary);
    }

    &:hover,
    &.router-link-active {
      color: map-get($fontColors, primary-hover);

      background-color: map-get($backgroundColors, primary-hover);

      &::v-deep(.ui-sprite-icon) {
        fill: map-get($fontColors, primary-hover);
      }
    }
  }
}
</style>
