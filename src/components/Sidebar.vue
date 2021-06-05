<script setup lang="ts" xmlns="http://www.w3.org/1999/html">
import {useI18n} from 'vue-i18n'

const {t} = useI18n()
</script>

<template>
  <div class="p-4 sm:w-72 mb-8 sm:mb-0 border-b sm:border-r border-gray-200 dark:border-gray-800">
    <ul>
      <SidebarItem to="/docs">{{ t('docs.get-started') }}</SidebarItem>
      <SidebarItem to="/installation">{{ t('docs.installation') }}</SidebarItem>
      <SidebarItem to="/channels">{{ t('docs.channels') }}</SidebarItem>
      <SidebarItem to="/resources">{{ t('docs.resources') }}</SidebarItem>
    </ul>
  </div>
</template>

<style scoped>
li {
  @apply w-full;
}

li a {
  @apply block p-2 font-bold rounded hover:bg-gray-200;
}
</style>
