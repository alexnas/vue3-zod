<script setup lang="ts">
import { RouterLink } from 'vue-router'
</script>

<template>
  <header class="flex items-center justify-between bg-gray-800 p-4">
    <img alt="Vue logo" src="@/assets/logo.svg" width="30" height="30" />

    <div>
      <nav class="flex gap-8 p-0">
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>
</template>

<style scoped></style>
