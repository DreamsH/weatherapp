<template>
  <main>
    <component :is="$route.meta.layout || 'div'"></component>
  </main>
</template>

<style lang="scss">
@import 'styles/app';
</style>
