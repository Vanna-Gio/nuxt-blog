<template>
  <div v-if="post">
    <h1>{{ post.title }}</h1>
    <p>{{ post.body }}</p>
  </div>
</template>

<script setup>
import { useHead } from '#imports'

useHead({
  title: post.value?.title,
  meta: [
    {
      name: 'description',
      content: post.value?.body.slice(0, 100)
    }
  ]
})
</script>

