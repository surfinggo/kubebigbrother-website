<script setup lang="ts">
import {useI18n} from 'vue-i18n'

const {t} = useI18n()
</script>

<template>
  <div class="my-6">
    <p>{{ t('get-started.p1') }}</p>
    <p>{{ t('get-started.p2') }}</p>
    <p><span class="mr-2">👉</span><a class="text-blue-500"
        href="https://github.com/spongeprojects/kubebigbrother-website" target="_blank">
      spongeprojects/kubebigbrother-website</a></p>
  </div>
</template>
