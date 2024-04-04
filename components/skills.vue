<template>
  <Section title="Навыки">
    <ul class="mb-1 mt-4 flex flex-wrap font-bold leading-relaxed">
      <li
        v-for="item of skills"
        :key="item"
        class="mb-1 mr-2 bg-gray-800 p-1.5 px-3 leading-relaxed text-white print:bg-white"
      >
        {{ item }}
      </li>
    </ul>
  </Section>
</template>

<script setup lang="ts">
const { skills } = defineProps<{ skills: string[] }>()
</script>
