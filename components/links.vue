<template>
  <section class="mb-0 mt-4 pb-2 first:mt-0">
    <!-- To keep in the same column -------------------------------------------------------------------------->
    <section class="break-inside-avoid">
      <section class="mb-2 break-inside-avoid border-b-4 border-gray-300 pb-4">
        <ul class="list-inside pr-7">
          <li
            v-for="link of links"
            :key="link.href"
            class="text-md print: mt-1 leading-normal text-black text-gray-500 transition duration-100 ease-in hover:text-gray-700"
          >
            <a :href="link.href" target="_blank" class="group">
              <span
                class="leading-snugish mr-2 text-lg font-semibold text-gray-700"
              >
                {{ link.name }}:
              </span>
              {{ link.text }}
              <span
                class="print: inline-block font-normal text-black text-gray-500 transition duration-100 ease-in group-hover:text-gray-700 print:text-black"
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
const links = [
  {
    href: 'https://t.me/alekhin_vv',
    name: 'Telegram',
    text: '@alekhin_vv',
  },
  {
    href: 'mailto:alekhin.v99@gmail.com',
    name: 'EMail',
    text: 'alekhin.v99@gmail.com',
  },
  {
    href: 'https://github.com/ValentinAlekhin',
    name: 'GitHub',
    text: 'github.com/ValentinAlekhin',
  },
]
</script>
