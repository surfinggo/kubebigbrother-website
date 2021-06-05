<script setup lang="ts">
import {useI18n} from 'vue-i18n'

const {t} = useI18n()
</script>

<template>
  <div class="text-center">
    <div class="fcc mb-8">
      <div class="max-w-100">
        <img src="/icon-128x128.png" class=""/>
      </div>
    </div>
    <div
        class="text-4xl sm:text-6xl lg:text-7xl leading-none font-extrabold tracking-tight mb-8">
      {{ t('index.desc') }}
    </div>
    <div class="mb-16">
      <a href="http://kubebigbrother-demo.spongeprojects.com/"
         target="_blank"
         class="btn btn-xl mr-2">{{ t('index.live-demo') }}</a>
      <router-link to="/docs" class="btn btn-xl">{{ t('index.get-started') }}</router-link>
    </div>
    <div class="grid grid-cols-12 gap-5 mb-16 px-5 md:px-5 lg:px-10">
      <div class="feature">
        <div class="title"><span class="icon">☸️</span>{{ t('index.feat-events') }}</div>
        <div class="desc">{{ t('index.desc-events') }}</div>
      </div>
      <div class="feature">
        <div class="title"><span class="icon">🔩</span>{{ t('index.feat-crd') }}</div>
        <div class="desc">{{ t('index.desc-crd') }}</div>
      </div>
      <div class="feature">
        <div class="title"><span class="icon">🔭</span>{{ t('index.feat-watch') }}</div>
        <div class="desc">{{ t('index.desc-watch') }}</div>
      </div>
      <div class="feature">
        <div class="title"><span class="icon">💌</span>{{ t('index.feat-notification') }}</div>
        <div class="desc">{{ t('index.desc-notification') }}</div>
      </div>
      <div class="feature">
        <div class="title"><span class="icon">🤗</span>{{ t('index.feat-channels') }}</div>
        <div class="desc">{{ t('index.desc-channels') }}</div>
      </div>
      <div class="feature">
        <div class="title"><span class="icon">👀</span>{{ t('index.feat-brother') }}</div>
        <div class="desc">{{ t('index.desc-brother') }}</div>
      </div>
    </div>
    <div class="fcc mb-5">
      <div class="">
        <img src="/screen-shot.png" class="rounded-lg"/>
      </div>
    </div>
    <div class="fcc mb-5">
      <div class="">
        <img src="/screen-shot-event-detail.png" class="rounded-lg"/>
      </div>
    </div>
  </div>
</template>

<style scoped>
.feature {
  @apply col-span-12 sm:col-span-6 md:col-span-4 mb-5
  text-left;
}

.title {
  @apply mb-2 text-xl;
}

.icon {
  @apply mr-2;
}

.desc {
  @apply text-gray-500 dark:text-gray-500;
}
</style>


<route lang="yaml">
meta:
  layout: home
</route>
