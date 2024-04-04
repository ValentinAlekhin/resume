<template>
  <Section title="Навыки">
    <ul
      class="text-md -mr-1.6 -mb-1 mt-4 flex flex-wrap font-bold leading-relaxed"
    >
      <li
        v-for="item of list"
        :key="item"
        class="print:border-inset mb-1 mr-2 bg-gray-800 p-1.5 px-3 leading-relaxed text-white print:bg-white"
      >
        {{ item }}
      </li>
    </ul>
  </Section>
</template>

<script setup lang="ts">
const list = [
  'JavaScript',
  'TypeScript',
  'Golang',
  'HTML',
  'CSS',
  'Nuxt 2/3',
  'React',
  'Electron',
  'WebSocket',
  'SCSS',
  'Tailwind',
  'NestJs',
  'PostgreSQL',
  'MongoDB',
  'GRpc',
  'Docker',
  'Nginx',
  'Linux',
  'GitHub Actions',
  'GitLab Ci',
]
</script>
