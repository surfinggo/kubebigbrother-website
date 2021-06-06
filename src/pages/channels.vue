<script setup lang="ts">
import {useI18n} from 'vue-i18n'
import channels from './channels_1.md'

const {t} = useI18n()
</script>

<template>
  <div class="my-6">
    <channels/>
    <p class="mt-3">{{ t('channels.p1') }}</p>
  </div>
</template>
