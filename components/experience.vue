<template>
  <Section title=" Опыт работы">
    <section
      v-for="(job, i) of jobs"
      :key="i"
      class="mb-2 break-inside-avoid border-b-2 border-gray-300 last:border-b-0"
    >
      <header>
        <h3 class="text-md leading-snugish font-semibold text-gray-800">
          {{ job.position }}
        </h3>
        <p class="text-sm leading-normal text-gray-500">
          {{ job.start }} &ndash; {{ job.end }} | {{ job.companyName }}
        </p>
      </header>
      <ul class="text-md leading-snugish mt-2 pl-3 font-normal text-gray-700">
        <li v-for="item in job.list" :key="item">
          <span class="-translate-y-px select-none text-gray-500">
            &rsaquo;
          </span>
          {{ item }}
        </li>
      </ul>
    </section>
  </Section>
</template>

<script lang="ts" setup>
const jobs = [
  {
    position: 'Fullstack Developer',
    start: 'Ноябрь 2021',
    end: 'По настоящее время',
    companyName: 'Нетсофт',
    list: [
      'Разработка микросервисов на NestJs с использованием gRpc',
      'Внедрение бизнес-процесса на движке Zeebe',
      'Поддержка монолитного сервера на NestJs',
      'Разработка приложения на Nuxt 2 для управления медиа-контентом',
      'Проектирование и разработка приложения на Electron + Nuxt 3 для отображения медиаконтента',
      'Автоматизация сборок Electron с помощью GitLab Ci',
      'Разработка панели администратора на React-Admin',
    ],
  },
  {
    position: 'Fullstack Developer',
    start: 'Май 2021',
    end: 'Октябрь 2021',
    companyName: 'ОПЗ МЭИ',
    list: [
      'Разработка сервера на TypeScript и Express с MongoDB и приложение на Vue 3',
      'Создание и поддержка GitHub Action CI/CD для проекта',
      'Развертывание на Unix-подобных системах с Docker и Nginx',
      'Введение новых разработчиков в проект',
    ],
  },
]
</script>
