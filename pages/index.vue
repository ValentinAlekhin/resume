<template>
  <Card>
    <Header v-bind="data.header" />
    <section>
      <Links :links="data.links" />
      <Summary :summary="data.summary" />
      <Experience :experience="data.experience" />
      <PetProjects :projects="data.projects" />
      <Skills :skills="data.skills" />
    </section>
  </Card>
</template>
<script setup lang="ts">
const data = await queryContent('/data').findOne()

useHead({
  title: data.title,
})

useSeoMeta({
  title: data.title,
  ogTitle: data.title,
  description: data.description,
  ogDescription: data.description,
})
</script>
