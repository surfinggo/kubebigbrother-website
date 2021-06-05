<script setup lang="ts">
import {useHead} from '@vueuse/head'
import {useI18n} from 'vue-i18n'
import {useStorage} from '@vueuse/core'

const {locale} = useI18n()
const localeRef = useStorage('locale', 'en')

locale.value = localeRef.value

// https://github.com/vueuse/head
// you can use this to manipulate the document head in any components,
// they will be rendered correctly in the html results with vite-ssg
useHead({
  title: 'Kubebigbrother',
  meta: [
    {name: 'description', content: 'Watch everything happens in the cluster'},
  ],
})


</script>

<template>
  <router-view/>
</template>
