
<template>
  <form
    class="w-11/12 md:w-1/2 my-6 mx-auto"
    action="https://formsubmit.co/fe0534e16eb7e999e8d2461ce48f3360" method="POST"
    v-if="!sent"
  >
  <!-- <h2>{{ error }}</h2> -->
   <input type="hidden" name="form-name" value="contact-us-form" />
    <h2 class="my-6 text-3xl text-center">Contact Us</h2>
    <p class="my-6 text-center">
      Please fill out this form and we will get
      back to you quickly.
    </p>

    <div class="grid xl:grid-cols-1 xl:gap-6">
      <div class="relative z-0 w-full mb-6 group">
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
          >Your Name</label
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

    <div class="grid xl:grid-cols-2 xl:gap-6">
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
  <div v-else>
    Thank you for sending the message, we'll get back to you soon soon!
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: '',
      details: '',
      name: '',
      phone: '',
      sent: false,
      error: "There's an issue!"
    }
  },
  methods: {
    async submit() {
    
      const url = "http://localhost:8888/.netlify/functions/send-email"
      // const url = "https://glowing-frangollo-c88705.netlify.app/.netlify/functions/send-email"
    const body = {
      email: this.email,
      name: this.name,
      details: `There's an email from someone! Their phone number is ${ this.phone } and they said: ${ this.details }`
    }
    console.log(body)
    // return
      const send = await this.$axios.post(url, body)
      .then(data => {
        if (data.status == 200) {
          this.sent = true;
        }
      })
      .catch(err => console.log(err))
    },
  },
};
</script>

<style scoped>
form {
  min-height: 50vh;
}
</style>