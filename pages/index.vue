<template>
<div>
  <div class="flex justify-around items-center mt-10 md:pl-24 md:my-10 w-full md:w-11/12 mx-auto">
    <HeroImage class="pl-3"/>
    <CTAButton /> 
  </div>
    <HomeInfo />
  </div>
</template>

<script>
import HeroImage from "~/assets/heroImage.svg?inline"

export default {
  components: {
    HeroImage,
},
  layout: 'default',
}
</script>


<style>
</style>