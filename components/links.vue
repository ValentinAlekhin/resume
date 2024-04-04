<template>
  <section class="mb-0 mt-4 pb-2 first:mt-0">
    <section class="break-inside-avoid">
      <section class="mb-2 break-inside-avoid border-b-4 border-gray-300 pb-4">
        <ul class="list-inside pr-7">
          <li
            v-for="link of links"
            :key="link.href"
            class="print: mt-1 leading-normal text-gray-500 transition duration-100 ease-in hover:text-gray-700"
          >
            <a :href="link.href" target="_blank" class="group">
              <span
                class="leading-snugish mr-2 text-lg font-semibold text-gray-700"
              >
                {{ link.name }}:
              </span>
              {{ link.text }}
              <span
                class="inline-block font-normal text-gray-500 transition duration-100 ease-in group-hover:text-gray-700 print:text-black"
              >
                ↗
              </span>
            </a>
          </li>
        </ul>
      </section>
    </section>
  </section>
</template>
<script setup lang="ts">
const { links } = defineProps<{
  links: Array<{ href: string; name: string; text: string }>
}>()
</script>
