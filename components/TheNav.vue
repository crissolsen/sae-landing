<template>
  <nav class="w-full flex justify-between border-b-2 p-4">
    <div class="flex items-center md:gap-4">
      <!-- Logo and title -->
      <SAELogo class="h-12 w-auto cursor-pointer" @click="$router.push('/')"/>
      <h1 class="text-lg md:text-2xl text-center py-2">Sedgefield Academy of Excellence</h1>
    </div>
    <!-- Fullscreen links -->
    <div class="items-center hidden md:flex">
      <!-- Links to other pages -->
      <ul class="hidden md:flex" >
        <li v-for="link in links" :key="link.id" @click="$router.push(link.link)">
          <NuxtLink :to="link.link">{{ link.title }}</NuxtLink>
        </li>
      </ul>
    </div>
    <!-- Mobile menu -->
    <div class="flex flex-wrap flex-column items-center md:hidden relative ">
      <svg viewBox="0 0 100 80" width="40" height="40" @mouseover="showLinks = !showLinks">
        <rect width="100" height="20"></rect>
        <rect y="30" width="100" height="20"></rect>
        <rect y="60" width="100" height="20"></rect>
      </svg>
      <ul v-if="showLinks" class="absolute top-full w-36 right-1/2 z-20 bg-white bg-opacity-80 rounded text-center transition">
        <li v-for="link in links" :key="link.id" @click="$router.push(link.link)">
          <NuxtLink :to="link.link" v-if="!link.cta">{{ link.title }}</NuxtLink>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
import SAELogo from "~/assets/logo.svg?inline";

export default {
  components: {
    SAELogo
},
  data() {
    return {
      links: [
        {
          id: 0,
          title: "Home",
          link: "/"
        },
        {
          id: 1,
          title: "About Us",
          link: "about-us",
        },
        {
          id: 2,
          title: "Contact Us",
          link: "contact",
        },
        {
          id: 3,
          title: "Apply Now",
          link: 'enroll'
        }
      ],
      showLinks: false
    };
  },
  watch: {
    $route: function() {
      this.showLinks = false;
    }
  }
};
</script>

<style scoped>
li {
  @apply rounded bg-blue-500 px-2 py-3 m-2 shadow-lg cursor-pointer hover:bg-blue-200 text-white hover:text-black transform transition hover:translate-y-1;
}
</style>
