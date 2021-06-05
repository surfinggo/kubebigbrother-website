<script setup lang="ts" xmlns="http://www.w3.org/1999/html">
import {useI18n} from 'vue-i18n'

const {t} = useI18n()
</script>

<template>
  <nav class="w-full text-xl text-center pb-8">
    <a class="mx-2" href="https://kubebigbrother.spongeprojects.com/" target="_blank"
       title="Kubebigbrother">
      <carbon-campsite/>
    </a>

    <a class="mx-2" href="https://twitter.com/wbsnail" target="_blank"
       title="Twitter">
      <carbon-logo-twitter/>
    </a>

    <a class="mx-2" href="https://github.com/spongeprojects/kubebigbrother" target="_blank"
       title="GitHub">
      <carbon-logo-github/>
    </a>
  </nav>
</template>
