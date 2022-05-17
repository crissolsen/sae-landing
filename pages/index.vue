<template>
  <div class="flex justify-around items-center my-5 md:pl-24 md:my-10 w-full md:w-11/12 mx-auto">
    <HeroImage />
    <CTAButton />
  </div>
</template>

<script>

import HeroImage from "~/assets/heroImage.svg?inline"
export default {
  components: {
    HeroImage
  },
  layout: 'default',
}
</script>


<style>
.svg-animate {
  animation: breathe 2s linear infinite;
  transform: translate(-121.63 -93.4);
}

@keyframes breathe {
  from {
    /* transform: scale(0.9) */
  }
  to {
    /* transform: scale(1) */
  }
}
</style>