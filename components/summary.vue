<template>
  <Section title="Обо мне">
    <p class="text-md my-2 leading-normal text-gray-700">
      {{ summary }}
    </p>
  </Section>
</template>
<script setup lang="ts">
const { summary } = defineProps<{ summary: string }>()
</script>
