<script setup lang="ts"></script>

<template>
  <form onsubmit="">
    <div class="flex flex-col space-y-6 px-4 text-base leading-6">
      <div>
        <label class="block" for="username">Name</label>
        <input
          class="mt-2 w-full border-2 border-gray-300 p-1"
          id="username"
          type="text"
          name="username"
          placeholder="Name"
        />
      </div>
      <div>
        <label class="block" for="password">Password</label>
        <input
          class="mt-2 w-full border-2 border-gray-300 p-1"
          id="password"
          type="password"
          name="password"
          placeholder="Password"
        />
      </div>
      <div class="relative">
        <button
          type="submit"
          class="mt-6 w-full items-center justify-center rounded-md px-8 py-2 text-base text-white transition duration-150 ease-in-out focus:outline-none focus:ring-2 focus:ring-teal-700 focus:ring-offset-2 enabled:bg-teal-700 enabled:hover:bg-teal-600 disabled:bg-gray-400 sm:rounded-lg"
        >
          Submit
        </button>
      </div>
    </div>
  </form>
</template>
