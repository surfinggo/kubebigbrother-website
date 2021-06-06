<script setup lang="ts">
import {useI18n} from 'vue-i18n'

const {t} = useI18n()
</script>

<template>
  <div class="my-6">
    <p>{{ t('installation.p1') }}</p>
  </div>
</template>
