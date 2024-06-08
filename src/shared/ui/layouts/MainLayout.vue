<template>
  <div class="main-layout">
    <slot name="header" />
    <slot name="navbar" />
    <slot />
    <slot name="footer" />
  </div>
</template>

<style scoped>
.main-layout {
  height: 100vh;
}
</style>
