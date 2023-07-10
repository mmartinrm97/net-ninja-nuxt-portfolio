<template>
  <section>
    <h1 class="mt-20 text-5xl font-bold">🙌🏻 Hello, I'm Miguel Miller</h1>
    <p class="p-2 text-base italic text-gray-900">
      FullStack developer Advocate at Laravel, Adonis JS and VueJs!
    </p>
  </section>
  <section class="flex flex-col md:flex-row">
    <div class="text-justify md:w-3/4">
      <h2 class="mt-8 text-3xl font-bold">My Story</h2>
      <p class="py-2 text-lg">
        Bachiller en la carrera profesional de Ingeniería de Sistemas de la
        Universidad Nacional de Cañete, con disposición a cumplir con las
        distintas funciones, obligaciones y normas laborales que tengan
        establecidas. Me presento con gran entusiasmo a esta institución para
        formar parte del cumplimiento de las metas planteadas en su misión.
      </p>
      <p class="py-2 text-lg">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. At beatae et
        facilis libero nam, pariatur perferendis sunt velit vitae voluptatem!
      </p>
      <p class="py-2 text-lg">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto
        beatae error excepturi fugiat illo in ipsum iste itaque minus modi,
        neque nulla odio odit perferendis quibusdam, repudiandae sint veniam
        veritatis!
      </p>
    </div>
    <div class="mx-auto flex w-1/2 items-center p-8 md:max-w-sm">
      <img
        alt=""
        class="w-full rounded-2xl object-cover"
        src="~/assets/images/Foto-Miguel-Ramos-Miller.png"
      />
    </div>
  </section>
  <section>
    <h2 class="mt-8 text-3xl font-bold">Latest Blog Posts</h2>
    <section class="grid md:grid-cols-3 mt-8 gap-10">
      <ThePosts :posts="posts"/>
    </section>
  </section>
</template>

<script setup>
const { data: posts } = await useAsyncData("latest-posts", () =>
  queryContent("/blog").sort({ data: 1 }).limit(3).find()
);
</script>

<style lang="scss" scoped></style>
