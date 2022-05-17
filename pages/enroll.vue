
<template>
  <form
    class="w-11/12 md:w-1/2 my-6 mx-auto"
    name="vue-tea"
    action="#"
    method="post"
    data-netlify="true"
    data-netlify-honeypot="bot-field"
    netlify
  >
   <input type="hidden" name="form-name" value="vue-tea" />
    <h2 class="my-6 text-3xl text-center">Start Enrollment</h2>
    <p class="my-6 text-center">
      Please fill out this form to start the enrollment process and we will get
      back to you quickly.
    </p>

    <div class="grid xl:grid-cols-2 xl:gap-6">
      <div class="relative z-0 w-full mb-6 group">
        <input
          type="text"
          name="floating_first_name"
          id="floating_first_name"
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
          for="floating_first_name"
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
          >First name</label
        >
      </div>
      <div class="relative z-0 w-full mb-6 group">
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
      </div>
    </div>
    <div class="relative z-0 mb-6 group">
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
    </div>

    <div class="grid xl:grid-cols-2 xl:gap-6">
      <div class="relative z-0 w-full mb-6 group">
        <input
          type="tel"
          name="floating_phone"
          id="floating_phone"
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
          for="floating_phone"
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
          name="floating_email"
          id="floating_company"
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
          for="floating_email"
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
    </div>
    <div class="w-full flex justify-center">
      <button
        type="submit"
        class="
          w-full
          md:w-1/2
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
        Submit
      </button>
    </div>
  </form>
</template>

<script>
export default {
  methods: {
    submit() {
      console.log("Submitted.");
    },
  },
};
</script>