 <script setup lang="ts">
const route = useRoute()
const slug = route.params.slug as string

const { data: post } = await useAsyncData(`blog-${slug}`, () =>
  queryCollection('blog').path(`/blog/${slug}`).first()
)
</script>

<template>
  <div v-if="post">
    <h1>{{ post.title }}</h1>
    <time>{{ post.date }}</time>
    <ContentRenderer :value="post" />
    <NuxtLink to="/blog">Tilbake til bloggen</NuxtLink>
  </div>
  <div v-else>
    <h1>Fant ikke artikkelen</h1>
    <NuxtLink to="/blog">Tilbake til bloggen</NuxtLink>
  </div>
</template>

<style scoped>



</style>

