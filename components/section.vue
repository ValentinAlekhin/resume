<template>
  <section
    class="mb-4 mt-0 break-inside-avoid border-b-4 border-gray-300 pb-6 first:mt-0 last:border-b-0 last:pb-2"
  >
    <section class="break-inside-avoid">
      <h2
        class="mb-2 text-xl font-black tracking-widest text-gray-800 print:font-normal"
      >
        {{ props.title }}
      </h2>
      <section class="mb-0 break-inside-avoid">
        <slot />
      </section>
    </section>
  </section>
</template>

<script setup lang="ts">
const props = defineProps<{ title: string }>()
</script>
