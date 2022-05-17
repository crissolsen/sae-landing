<template>
  <button
    class="
      md:text-2xl
      bg-blue-700
      text-white
      rounded-xl
      shadow-lg
      hover:bg-blue-200 hover:translate-y-1 hover:text-black
      transform
      transition
      px-2
      md:px-6
      py-4
      relative
      right-20
      w-full
      md:w-1/5
    "
    @click="$router.push('enroll')"
  >
    Enroll Now
  </button>
</template>