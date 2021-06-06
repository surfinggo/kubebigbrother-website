<script setup lang="ts">
import {useI18n} from 'vue-i18n'
import resource from './resource_1.md'

const {t} = useI18n()
</script>

<template>
  <div class="my-6">
    <resource/>
    <p class="mt-3">{{ t('resources.p1') }}</p>
  </div>
</template>
