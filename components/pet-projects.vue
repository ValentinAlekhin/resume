<template>
  <Section title="Личные проекты">
    <section
      v-for="(project, i) of list"
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
const list = [
  {
    name: 'Приложение для ведения личного бюджета',
    href: 'https://budget.nikadmitrieva.ru/',
    description:
      'Цель приложения — помочь мне вести личный бюджет в удобной для меня форме. На данный момент оно позволяет записывать доходы и расходы, просматривать и редактировать записи и наблюдать за статистикой. Фронтенд написан на Nuxt 3, бекенд сейчас работает на NodeJs(NestJs), но переписывается на Golang(Gin).',
    source: 'https://github.com/ValentinAlekhin/budget',
  },
  {
    name: 'Сайт портофилио фотографа',
    href: 'https://nikadmitrieva.ru/',
    description:
      'Портфолио для девушки фотографа. Клиент написан на Nuxt 2 в качетве бека выбран Strapi.',
    source: 'https://github.com/ValentinAlekhin/nikadmitrieva-new',
  },
]
</script>
