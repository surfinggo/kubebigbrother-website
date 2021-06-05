<script setup lang="ts">

</script>

<template>
  <main class="flex flex-col items-center px-4 text-gray-900 dark:text-gray-200 transition-colors duration-200">
    <Nav/>
    <div class="max-w-256">
      <router-view/>
    </div>
    <Footer/>
  </main>
</template>
