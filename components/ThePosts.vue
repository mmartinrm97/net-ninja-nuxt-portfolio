<template>
  <div
    v-for="post in props.posts"
    class="overflow-hidden rounded-lg bg-white shadow-md hover:opacity-75"
  >
    <NuxtLink :to="post._path">
      <img
        :src="`/images/blog/${post.cover}`"
        alt="Blog Post Cover Image"
        class="h-48 w-full object-cover"
      />
    </NuxtLink>
    <div class="p-6">
      <h2 class="mb-2 text-xl font-bold">{{ post.title }}</h2>
      <p class="mb-4 text-gray-700">{{ post.description }}</p>
      <NuxtLink
        :to="post._path"
        class="float-right mb-8 inline-block rounded bg-blue-500 px-4 py-2 text-white hover:bg-blue-700"
      >
        Read More
      </NuxtLink>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  posts: {
    type: Array,
    required: true,
  },
});
</script>

<style lang="scss" scoped></style>
