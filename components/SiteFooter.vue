<template>
  <footer class="bg-gray-800">
    <section
      class="mx-auto flex max-w-7xl flex-row px-2 text-gray-300 sm:px-4 lg:py-6"
    >
      <p class="flex flex-1 items-center">
        &copy; Miguel Ramos Miller 2023. All Rights Reserved
      </p>
      <div class="mb-4 mt-2 flex flex-row justify-center gap-4">
        <a v-for="link in links" :key="link.name" :href="link.href">
          <Icon
            :name="link.icon"
            class="text-gray-300 transition-colors hover:text-gray-100"
            size="1.5rem"
          />
        </a>
      </div>
    </section>
  </footer>
</template>

<script setup>
const links = [
  {
    name: "Github",
    href: "http://github.com",
    icon: "mdi:github",
  },
  {
    name: "Twitter",
    href: "http://twitter.com",
    icon: "mdi:twitter",
  },
  {
    name: "Facebook",
    href: "http://facebook.com",
    icon: "mdi:facebook",
  },
  {
    name: "LinkedIn",
    href: "http://linkedin.com",
    icon: "mdi:linkedin",
  },
  {
    name: "Instagram",
    href: "http://instagram.com",
    icon: "mdi:instagram",
  },
];
</script>

<style lang="scss" scoped></style>
