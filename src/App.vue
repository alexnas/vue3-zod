<script setup lang="ts">
import { RouterView } from 'vue-router'
import AppHeader from './components/AppHeader.vue'
</script>

<template>
  <div class="font-roboto flex h-screen flex-col bg-gray-200">
    <app-header />
    <router-view />
  </div>
</template>
