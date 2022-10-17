
<template>
  <form
    class="w-11/12 md:w-1/2 mt-6 mx-auto max-w-md"
    action="https://formsubmit.co/sedge.ae@gmail.com"
    method="POST"
    v-if="!sent"
  >
    <!-- <h2>{{ error }}</h2> -->
    <input type="hidden" name="form-name" value="contact-us-form" />
    <h2 class="my-6 text-3xl text-center">Contact Us</h2>

    <div class="grid xl:grid-cols-auto xl:gap-6">
      <div class="relative z-0 w-full mb-10 group">
        <input
          type="text"
          name="enquiry-name"
          id="enquiry-name"
          class="
            block
            py-2.5
            px-0
            w-full
            text-gray-900
            bg-transparent
            border-0 border-b-2 border-gray-300
            appearance-none
            dark:text-white dark:border-gray-600 dark:focus:border-blue-500
            focus:outline-none focus:ring-0 focus:border-blue-600
            peer
          "
          placeholder=" "
          required=""
          v-model="name"
        />
        <label
          for="enquiry-name"
          class="
            peer-focus:font-medium
            absolute
            text-gray-500
            dark:text-gray-400
            duration-300
            transform
            -translate-y-6
            scale-80
            top-3
            -z-10
            origin-[0]
            peer-focus:left-0
            peer-focus:text-blue-600
            peer-focus:dark:text-blue-500
            peer-placeholder-shown:scale-100
            peer-placeholder-shown:translate-y-0
            peer-focus:scale-85 peer-focus:-translate-y-6
          "
          >Name</label
        >
      </div>
      <!-- <div class="relative z-0 w-full mb-6 group">
        <input
          type="text"
          name="floating_last_name"
          id="floating_last_name"
          class="
            block
            py-2.5
            px-0
            w-full
            text-gray-900
            bg-transparent
            border-0 border-b-2 border-gray-300
            appearance-none
            dark:text-white dark:border-gray-600 dark:focus:border-blue-500
            focus:outline-none focus:ring-0 focus:border-blue-600
            peer
          "
          placeholder=" "
          required=""
        />
        <label
          for="floating_last_name"
          class="
            peer-focus:font-medium
            absolute
            text-gray-500
            dark:text-gray-400
            duration-300
            transform
            -translate-y-6
            scale-80
            top-3
            -z-10
            origin-[0]
            peer-focus:left-0
            peer-focus:text-blue-600
            peer-focus:dark:text-blue-500
            peer-placeholder-shown:scale-100
            peer-placeholder-shown:translate-y-0
            peer-focus:scale-80 peer-focus:-translate-y-6
          "
          >Last name</label
        >
      </div> -->
    </div>
    <!-- <div class="relative z-0 mb-6 group">
      <input
        name="floating_student"
        class="
          block
          py-2.5
          px-0
          w-full
          text-gray-900
          bg-transparent
          border-0 border-b-2 border-gray-300
          appearance-none
          dark:text-white dark:border-gray-600 dark:focus:border-blue-500
          focus:outline-none focus:ring-0 focus:border-blue-600
          peer
        "
        placeholder=" "
        required=""
        v-model="details"
      />
      <label
        for="floating_student"
        class="
          peer-focus:font-medium
          absolute
          text-gray-500
          dark:text-gray-400
          duration-300
          transform
          -translate-y-6
          scale-80
          top-3
          -z-10
          origin-[0]
          peer-focus:left-0
          peer-focus:text-blue-600
          peer-focus:dark:text-blue-500
          peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0
          peer-focus:scale-80 peer-focus:-translate-y-6
        "
        >Prospective Student(s) and Grade(s)</label
      >
    </div> -->

    <div class="grid xl:grid-cols-auto xl:gap-6">
      <div class="relative z-0 w-full mb-6 group">
        <input
          type="tel"
          name="phone"
          id="phone"
          class="
            block
            py-2.5
            px-0
            w-full
            text-gray-900
            bg-transparent
            border-0 border-b-2 border-gray-300
            appearance-none
            dark:text-white dark:border-gray-600 dark:focus:border-blue-500
            focus:outline-none focus:ring-0 focus:border-blue-600
            peer
          "
          placeholder=" "
          required=""
          v-model="phone"
        />
        <label
          for="phone"
          class="
            peer-focus:font-medium
            absolute
            text-gray-500
            dark:text-gray-400
            duration-300
            transform
            -translate-y-6
            scale-80
            top-3
            -z-10
            origin-[0]
            peer-focus:left-0
            peer-focus:text-blue-600
            peer-focus:dark:text-blue-500
            peer-placeholder-shown:scale-100
            peer-placeholder-shown:translate-y-0
            peer-focus:scale-80 peer-focus:-translate-y-6
          "
          >Phone number
        </label>
      </div>
      <div class="relative z-0 w-full mb-6 group">
        <input
          type="email"
          name="email"
          id="email"
          class="
            block
            py-2.5
            px-0
            w-full
            text-gray-900
            bg-transparent
            border-0 border-b-2 border-gray-300
            appearance-none
            dark:text-white dark:border-gray-600 dark:focus:border-blue-500
            focus:outline-none focus:ring-0 focus:border-blue-600
            peer
          "
          placeholder=" "
          required=""
          v-model="email"
        />
        <label
          for="email"
          class="
            peer-focus:font-medium
            absolute
            text-gray-500
            dark:text-gray-400
            duration-300
            transform
            -translate-y-6
            scale-80
            top-3
            -z-10
            origin-[0]
            peer-focus:left-0
            peer-focus:text-blue-600
            peer-focus:dark:text-blue-500
            peer-placeholder-shown:scale-100
            peer-placeholder-shown:translate-y-0
            peer-focus:scale-80 peer-focus:-translate-y-6
          "
          >Email</label
        >
      </div>
      <div class="relative z-0 w-full mb-6 group">
        <textarea
          name="details"
          v-model="details"
          id="details"
          class="
            block
            py-2.5
            px-0
            w-full
            text-gray-900
            bg-transparent
            border-0 border-b-2 border-gray-300
            dark:text-white dark:border-gray-600 dark:focus:border-blue-500
            focus:outline-none focus:ring-0 focus:border-blue-600
            peer
          "
        >
        </textarea>
        <label
          for="details"
          class="
            peer-focus:font-medium
            absolute
            text-gray-500
            dark:text-gray-400
            duration-300
            transform
            -translate-y-6
            scale-80
            top-3
            -z-10
            origin-[0]
            peer-focus:left-0
            peer-focus:text-blue-600
            peer-focus:dark:text-blue-500
            peer-placeholder-shown:scale-100
            peer-placeholder-shown:translate-y-0
            peer-focus:scale-80 peer-focus:-translate-y-6
          "
          >Message
        </label>
      </div>
    </div>
    <div class="w-full flex justify-center">
      <button
        type="submit"
        class="submit-button"
      >
        Submit
      </button>
    </div>
  </form>
  <div v-else>
    Thank you for sending the message, we'll get back to you soon soon!
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: "",
      details: "",
      name: "",
      phone: "",
      sent: false,
      error: "There's an issue!",
    };
  },
};
</script>

<style scoped>
form {
  min-height: 50vh;
}
</style>