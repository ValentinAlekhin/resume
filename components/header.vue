<template>
  <header
    class="mb-2 inline-flex w-full items-baseline justify-between border-b-4 border-gray-300 align-top"
  >
    <section class="block">
      <h1 class="mb-0 text-3xl font-bold text-gray-700 md:text-5xl">
        {{ name }}
      </h1>
      <h2 class="m-0 ml-2 text-xl font-semibold text-gray-700 md:text-2xl">
        {{ profession }}
      </h2>
      <h3 class="m-0 ml-2 mt-2 text-xl font-semibold text-gray-500">
        {{ location }}
      </h3>
    </section>
    <section
      class="mb-5 mt-0 justify-between bg-gray-700 px-3 text-4xl font-black leading-none text-white print:bg-black"
      style="padding-bottom: 1.5rem; padding-top: 1.5rem"
    >
      <section
        v-for="letter of initial.split('')"
        :key="letter"
        class="text-center uppercase"
      >
        {{ letter }}
      </section>
    </section>
  </header>
</template>
<script setup lang="ts">
const { name, profession, location, initial } = defineProps<{
  name: string
  profession: string
  location: string
  initial: string
}>()
</script>
