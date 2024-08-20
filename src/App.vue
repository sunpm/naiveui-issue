<script setup lang="ts">
</script>

<template>
  <n-card title="卡片插槽示例">
    <template #header-extra>
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
      #header-extra
    </template>
    卡片内容
    <template #footer>
      #footer
    </template>
    <template #action>
      #action
    </template>
  </n-card>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
