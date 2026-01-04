<template>
  <div>
    <h1>Posts</h1>

    <ul>
      <li v-for="post in posts" :key="post.id">
        <NuxtLink :to="`/posts/${post.id}`">
          {{ post.title }}
        </NuxtLink>
      </li>
    </ul>
  </div>
</template>

<script setup>
const { data: posts } = await useFetch(
  'https://jsonplaceholder.typicode.com/posts?_limit=5'
)
</script>
