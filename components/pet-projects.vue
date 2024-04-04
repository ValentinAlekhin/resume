<template>
  <Section title="Личные проекты">
    <section
      v-for="(project, i) of projects"
      :key="i"
      class="mb-2 break-inside-avoid border-b-2 border-gray-300 pb-2 last:border-b-0"
    >
      <header>
        <h3 class="font-semibold text-gray-800">
          <a :href="project.href" target="_blank">
            <span class="mr-2 font-semibold"> {{ project.name }}</span>

            <span
              class="print: inline-block font-normal text-gray-500 transition duration-100 ease-in group-hover:text-gray-700 print:text-black"
            >
              ↗
            </span>
          </a>
        </h3>

        <a
          target="_blank"
          :href="project.source"
          class="text-sm leading-normal text-gray-500"
        >
          <span class="mr-2">Исходный код</span>

          <span
            class="inline-block font-normal text-gray-500 transition duration-100 ease-in group-hover:text-gray-700 print:text-black"
          >
            ↗
          </span>
        </a>
      </header>

      <p class="mt-2 text-gray-700">
        {{ project.description }}
      </p>
    </section>
  </Section>
</template>

<script lang="ts" setup>
const { projects } = defineProps<{
  projects: Array<{
    name: string
    href: string
    description: string
    source: string
  }>
}>()
</script>
