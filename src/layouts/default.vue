<script setup lang="ts">
import {useI18n} from "vue-i18n";
import { isDark, toggleDark } from '~/logic'

const {t, availableLocales, locale} = useI18n()

const toggleLocales = () => {
  // change to some real logic
  const locales = availableLocales
  locale.value = locales[(locales.indexOf(locale.value) + 1) % locales.length]
}
</script>

<template>
  <main class="px-4 text-gray-900 dark:text-gray-200 transition-colors duration-200">
    <div
        class="fcb border-b border-gray-200 dark:border-gray-800 mb-16 sm:mb-20 -mx-4 px-4 sm:mx-0 sm:px-0 transition-colors duration-200">
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
          <span class="hidden sm:inline">{{ t('docs') }}</span>
        </router-link>
        <span class="item" :title="t('button.toggle_dark')" @click="toggleDark">
          <carbon-moon v-if="isDark" />
          <carbon-sun v-else />
        </span>

        <span class="item" :title="t('button.toggle_langs')" @click="toggleLocales">
          <carbon-language />
        </span>
        <a
            href="https://github.com/spongeprojects/kubebigbrother" target="_blank"
            class="item text-lg">
          <carbon-logo-github/>
        </a>
      </div>
    </div>

    <router-view/>
    <Footer/>
  </main>
</template>

<style scoped>
.item {
  @apply flex items-center justify-center py-4 cursor-pointer;
}
</style>
