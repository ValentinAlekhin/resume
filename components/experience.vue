<template>
  <Section title=" Опыт работы">
    <section
      v-for="(job, i) of experience"
      :key="i"
      class="mb-2 break-inside-avoid border-b-2 border-gray-300 pb-2 last:border-b-0"
    >
      <header>
        <h3 class="font-semibold text-gray-800">
          {{ job.profession }}
        </h3>
        <p class="text-sm leading-normal text-gray-500">
          {{ job.start }} &ndash; {{ job.end }} | {{ job.company }}
        </p>
      </header>
      <ul class="mt-2 pl-3 font-normal text-gray-700">
        <li v-for="responsible in job.responsibilities" :key="responsible">
          <span class="-translate-y-px select-none text-gray-500">
            &rsaquo;
          </span>
          {{ responsible }}
        </li>
      </ul>
    </section>
  </Section>
</template>

<script lang="ts" setup>
const { experience } = defineProps<{
  experience: Array<{
    profession: number
    start: string
    end: string
    company: string
    responsibilities: string[]
  }>
}>()
</script>
