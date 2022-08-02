<template>
  <footer
    class="
      mt-16
      py-4
      flex flex-columns
      justify-center
      md:justify-between
      gap-4
      w-full
      md:w-3/4
      mx-auto
      border-t-2
      flex-wrap-reverse
      md:flex-no-wrap
    "
  >
  <div class="justify-self-start">Sedgefield Academy of Excellence <br />© 2022</div>
    <DocDownloads />

    <div class="w-64 md:w-80">
      <iframe
        src="https://maps.google.com/maps?q=Sedgefield%20Academy%20of%20Excellence&t=&z=15&ie=UTF8&iwloc=&output=embed"
        frameborder="0"
        scrolling="no"
        marginheight="0"
        marginwidth="0"
        class="w-full h-64"
      ></iframe>
    </div>
    <div>
      <h4 class="text-lg">Contact Details:</h4>
      <a href="tel:27834465508">Marcia 083 446 5508</a>
      <a href="tel:27849168429">Richard 084 916 8429</a>
      <a href="mailto:sedge.ae@gmail.com">Email: sedge.ae@gmail.com</a>
      <div class="flex gap-4 py-4">
        <a href="https://www.facebook.com/sedge.ae" target="_blank"
          ><Facebook
        /></a>
        <a href="https://wa.me/27834465508" target="_blank"><WhatsApp /></a>
      </div>
    </div>
  </footer>
</template>

<script>
import Facebook from "~/assets/fb.svg?inline";
import WhatsApp from "~/assets/whatsapp.svg?inline";

export default {
  components: {
    Facebook,
    WhatsApp,
  },
};
</script>

<style scoped>
a {
  @apply block text-blue-800;
}

svg {
  @apply w-10;
}
</style>