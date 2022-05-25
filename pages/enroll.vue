<template>
<div v-if="!success">
    {{ values }}

    {{ position }}

    {{ values2 }}
    <FormulateForm
    v-model="values"
    :schema="schemaOne"
    class="mx-auto w-11/12 md:w-1/2 max-w-md p-4 mt-10 rounded border-2 border-blue-200"
    v-if="position == 1"
    @submit="position = 2"
  />

  <FormulateForm
    v-model="values2"
    :schema="schemaTwo"
    class="mx-auto w-1/2 w-11/12 max-w-md p-4 mt-10 rounded border-2 border-blue-200"
    v-if="position == 2"
    @submit = "submitForm()"
  />

</div>
<div v-else>Thank you for your enrollment submission. We'll get back to you shortly.</div>
</template>

<script>
import schemaOne from "~/assets/enrollSchemaFirst.json"
import schemaTwo from "~/assets/enrollSchemaSecond.json"


export default {
    data() {
        return {
            values: {},
            values2: {},
            schemaOne,
            schemaTwo,
            position: 1,
            error: "",
            success: ""
        }
    },

    methods: {
        async submitForm() {
            let formInfo = {...this.values, ...this.values2 }

            this.$axios.defaults.headers.post['Content-Type'] = 'application/json'
            const submitForm = await this.$axios.post("https://formsubmit.co/fe0534e16eb7e999e8d2461ce48f3360", formInfo)
            .then(res => res.status == 200 ? this.success = true : this.error = "There was a problem!")
            .catch(e => console.log(e))


        }
    }
}
</script>

<style>
.labels {
    @apply text-lg;
}

.inputs {
    @apply border-2 rounded pl-2 focus:border-blue-400;
}

.errors {
    @apply text-sm text-red-800;
}

.submit-button {
    @apply w-full md:w-1/2 rounded bg-blue-500
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
}
</style>