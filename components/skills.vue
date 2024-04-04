<template>
  <section
    class="mb-4 mt-0 break-inside-avoid border-b-4 border-gray-300 pb-6 first:mt-0"
  >
    <!-- To keep in the same column -->
    <section class="break-inside-avoid">
      <h2
        class="mb-2 text-lg font-bold tracking-widest text-gray-700 print:font-normal"
      >
        Навыки
      </h2>
      <section class="mb-0 break-inside-avoid">
        <section class="mt-1 last:pb-1">
          <ul
            class="text-md -mr-1.6 -mb-1 flex flex-wrap font-bold leading-relaxed"
          >
            <li
              v-for="item of list"
              :key="item"
              class="mr-1.6 print:border-inset mb-1 bg-gray-800 p-1.5 leading-relaxed text-white print:bg-white"
            >
              {{ item }}
            </li>
          </ul>
        </section>
      </section>
    </section>
  </section>
</template>
<script setup lang="ts">
const list = ['HTML5', 'CSS3']
</script>
