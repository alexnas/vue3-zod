<script setup lang="ts">
import AuthFormContainer from '@/components/form/AuthFormContainer.vue'
import ViewContainer from '@/views/ViewContainer.vue'
import AuthForm from '@/components/form/AuthForm.vue'
</script>

<template>
  <main>
    <view-container title="Auth Form">
      <auth-form-container>
        <auth-form />
      </auth-form-container>
    </view-container>
  </main>
</template>
