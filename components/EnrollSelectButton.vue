<template>
  <button
    role="button"
    @click="$emit('selected', selection)"
    class="
      rounded
      bg-blue-500
      px-2
      py-3
      mx-auto
      shadow-lg
      cursor-pointer
      hover:bg-blue-200
      text-white
      hover:text-black
      transform
      transition
      hover:translate-y-1
      px-5
      py-2.5
      text-center
    "
  >
  {{ text }}</button>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
    },
    selection: {
      type: String,
    },
  },
};
</script>