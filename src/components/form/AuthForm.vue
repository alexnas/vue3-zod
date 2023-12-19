<script setup lang="ts">
import { useField, useForm } from 'vee-validate'
import { toTypedSchema } from '@vee-validate/zod'
import * as zod from 'zod'

const validationSchema = toTypedSchema(
  zod.object({
    username: zod.string().min(3).max(25),
    password: zod.string().min(5).max(25)
  })
)

const { handleSubmit, errors, meta } = useForm({
  validationSchema
})

const { value: username } = useField('username')
const { value: password } = useField('password')

const onSubmit = handleSubmit((values) => {
  alert(JSON.stringify(values, null, 2))
})
</script>

<template>
  <form @submit="onSubmit">
    <div class="flex flex-col space-y-6 px-4 text-base leading-6">
      <div>
        <label class="block" for="username">Name</label>
        <input
          class="mt-2 w-full border-2 border-gray-300 p-1"
          id="username"
          type="text"
          name="username"
          v-model="username"
          placeholder="Name"
        />
        <span class="flex justify-end text-sm text-orange-400">{{ errors.username }}</span>
      </div>

      <div>
        <label class="block" for="password">Password</label>
        <input
          class="mt-2 w-full border-2 border-gray-300 p-1"
          id="password"
          type="password"
          name="password"
          v-model="password"
          placeholder="Password"
        />
        <span class="flex justify-end text-sm text-orange-400">{{ errors.password }}</span>
      </div>
      <div class="relative">
        <button
          :disabled="!meta.dirty || !meta.valid"
          class="mt-6 w-full items-center justify-center rounded-md px-8 py-2 text-base text-white transition duration-150 ease-in-out focus:outline-none focus:ring-2 focus:ring-teal-700 focus:ring-offset-2 enabled:bg-teal-700 enabled:hover:bg-teal-600 disabled:bg-gray-400 sm:rounded-lg"
        >
          Submit;
        </button>
      </div>
    </div>
  </form>
</template>
