<script setup lang="ts">

</script>

<template>
  <main class="flex flex-col items-center text-gray-900 dark:text-gray-200 transition-colors duration-200">
    <Nav/>
    <div class="block sm:flex w-full" style="height: calc(100vh - 4rem - 1px)">
      <Sidebar/>
      <div class="flex flex-col items-center w-full">
        <div class="max-w-256 mb-16">
          <router-view/>
        </div>
        <Footer/>
      </div>
    </div>
  </main>
</template>

