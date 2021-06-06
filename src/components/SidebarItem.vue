<script lang="ts">
import {ref} from 'vue';

const to = ref('')

export default {
  props: {
    to,
  }
}
</script>

<template>
  <li>
    <router-link :to="to" :class="$route.fullPath === to ? 'active' : ''">
      <slot/>
    </router-link>
  </li>
</template>

<style scoped>
li {
  @apply w-full mb-1;
}

li a {
  @apply block p-2 font-bold rounded !hover:dark:bg-gray-700 !hover:bg-gray-300 transition-colors duration-200;
}

li a.active {
  @apply bg-gray-200 dark:bg-gray-800;
}
</style>
