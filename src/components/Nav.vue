<script setup lang="ts" xmlns="http://www.w3.org/1999/html">
import {useI18n} from 'vue-i18n'
import { isDark, toggleDark } from '~/logic'
import {useStorage} from '@vueuse/core'

const {t, availableLocales, locale} = useI18n()
const localeRef = useStorage('locale', 'en')

const toggleLocales = () => {
  const locales = availableLocales
  locale.value = locales[(locales.indexOf(locale.value) + 1) % locales.length]
  localeRef.value = locale.value
}
</script>

<template>
  <nav
      class="fcb w-full h-16 border-b border-gray-200 dark:border-gray-800
      px-4 transition-colors duration-200">
    <div class="max-w-48 sm:max-w-62">
      <router-link to="/">
        <img src="/icon-text-right-bg-transparent.png" class=""/>
      </router-link>
    </div>
    <div class="flex items-center space-x-4 sm:space-x-6">
      <router-link
          class="font-medium py-4"
          to="/docs">
        <span class="sm:hidden">{{ t('docs-short') }}</span>
        <span class="hidden sm:inline">{{ t('docs-long') }}</span>
      </router-link>
      <span class="item" :title="t('button.toggle_dark')" @click="toggleDark">
          <carbon-moon v-if="isDark"/>
          <carbon-sun v-else/>
        </span>

      <span class="item" :title="t('button.toggle_langs')" @click="toggleLocales">
          <carbon-language/>
        </span>
      <a
          href="https://github.com/spongeprojects/kubebigbrother" target="_blank"
          class="item text-lg">
        <carbon-logo-github/>
      </a>
    </div>
  </nav>
</template>

<style scoped>
.item {
  @apply flex items-center justify-center py-4 cursor-pointer;
}
</style>
