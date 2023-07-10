<template>
 <div>
   <ContentRenderer :value="data" class="prose mx-auto my-10 max-w-7xl" />

   <div class="my-8">
     <a
         v-for="tag in data.tags"
         :key="tag"
         :href="`/blog/tags/${tag}`"
         class="inline-block py-2 text-sm font-semibold px-4 rounded-lg text-gray-100 bg-blue-500 uppercase last:mr-0 mr-4"
     >
       <Icon name="mdi:tag" size="1.5rem" class="text-gray-100 mr-2"/>{{tag}}
     </a>
   </div>
 </div>
</template>

<script setup>
const { path } = useRoute();

const { data } = await useAsyncData(`content-${path}`, () => {
  return queryContent().where({ _path: path }).findOne();
});
</script>

<style scoped></style>
