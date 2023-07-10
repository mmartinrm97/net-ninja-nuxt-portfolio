<template>
  <h1 class="my-8 text-3xl">Blog Posts</h1>
 <p>
   Lorem ipsum doslor sit amet, consectetur adipisicing elit. Mollitia, placeat
   ratione. A adipisci aliquam animi aperiam consequuntur deserunt dignissimos
   dolor dolorem eligendi explicabo facere hic inventore itaque nemo obcaecati
   officia omnis placeat quae qui, quo sapiente similique, temporibus ullam! Ab,
   animi architecto doloremque ducimus eligendi enim, facere id illo molestiae
   non officia, rem temporibus vitae. Ab ad aperiam dolores eaque eius enim
   expedita facere id impedit in ipsum iure laudantium nisi obcaecati omnis
   pariatur perspiciatis qui quo, quod sequi totam, unde vel veritatis. Accusamus
   deleniti distinctio dolore magni minima non quod sed. Consequuntur deserunt
   dolorum exercitationem explicabo incidunt laborum quo!
 </p>

  <section class="grid md:grid-cols-3 mt-8 gap-10">
    <ThePosts :posts="posts"/>
  </section>

</template>

<script setup>
const { data: posts } = await useAsyncData("posts", () =>
  queryContent("/blog").find()
);
</script>

<style lang="scss" scoped></style>
