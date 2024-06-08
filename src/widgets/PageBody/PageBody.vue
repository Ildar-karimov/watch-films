<template>
<body class="page-body">
  <main class="page-body__inner">
    <slot />
  </main>
  <slot name="footer" />
</body>
</template>

<style scoped lang="scss">
@use '@/shared/assets/scss/consts/layoutVariables.scss' as *;

.page-body {
  padding-top: $headerHeight;
  padding-left: $sideBarWidth;
  height: 100%;
}

.page-body__inner {
  padding: 26px 18px;
  min-height: calc(100% - $footerHeight);
}
</style>