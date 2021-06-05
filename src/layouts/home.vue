<script setup lang="ts">

</script>

<template>
  <main class="flex flex-col items-center text-gray-900 dark:text-gray-200 transition-colors duration-200">
    <Nav/>
    <div class="max-w-256 my-16">
      <router-view/>
    </div>
    <Footer/>
  </main>
</template>
