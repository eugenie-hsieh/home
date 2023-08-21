<template>
  <div class="background">
    <main class="content">
      <slot />
    </main>
  </div>
</template>

<style scoped lang="scss">
.background {
  background-color: var(--layout-bg);
  padding: var(--layout-padding);

  .content {
    color: var(--white);
  }
}
</style>
