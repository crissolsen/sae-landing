<template>
  <div v-if="!success" style="min-height: 50vh">
  <!-- Use in dev if you want to see all forms -->
    <!-- <div
      class="bg-red-400 p-4 h-10 w-20 m-4"
      v-for="(showPosition, i) in possiblePositions"
      :key="i"
      @click="(position = showPosition), (applicationSelected = true)"
    >
      {{ showPosition }}
    </div> -->
    <div
      v-if="!applicationSelected"
      class="
        flex flex-wrap
        justify-center
        items-center
        max-w-3xl
        mx-auto
        gap-y-6
      "
    >
      <h2 class="text-xl w-full text-center py-4">
        Please select the application that applies
      </h2>
      <EnrollSelectButton
        text="Extra Lesson Learner"
        @selected="applicationType($event)"
        selection="extraLessons"
      />
      <EnrollSelectButton
        text="Casual Learner"
        @selected="applicationType($event)"
        selection="casualLearner"
      />
      <EnrollSelectButton
        text="Supplementary Learner"
        @selected="applicationType($event)"
        selection="supplementaryLearner"
      />
      <EnrollSelectButton
        text="Extended Learner"
        @selected="applicationType($event)"
        selection="extendedLearner"
      />
    </div>
    <div v-if="applicationSelected">
      <FormulateForm
        v-model="values"
        :schema="schemaA"
        class="
          mx-auto
          w-11/12
          md:w-1/2
          max-w-md
          p-4
          mt-10
          rounded
          border-2 border-blue-200
        "
        v-if="position == 'a'"
        @submit="checkPosition('a')"
      />

      <FormulateForm
        v-model="values2"
        :schema="schemaB"
        class="
          mx-auto
          w-1/2 w-11/12
          max-w-md
          p-4
          mt-10
          rounded
          border-2 border-blue-200
        "
        v-if="position == 'b'"
        @submit="checkPosition('b')"
      />

      <FormulateForm
        v-model="values3"
        :schema="schemaC"
        class="
          mx-auto
          w-1/2 w-11/12
          max-w-md
          p-4
          mt-10
          rounded
          border-2 border-blue-200
        "
        v-if="position == 'c'"
        @submit="checkPosition('c')"
      />

      <FormulateForm
        v-model="values4"
        :schema="schemaD"
        class="
          mx-auto
          w-1/2 w-11/12
          max-w-md
          p-4
          mt-10
          rounded
          border-2 border-blue-200
        "
        v-if="position == 'd'"
        @submit="checkPosition('d')"
      />

      <FormulateForm
        v-model="values5"
        :schema="schemaE"
        class="
          mx-auto
          w-1/2 w-11/12
          max-w-md
          p-4
          mt-10
          rounded
          border-2 border-blue-200
        "
        v-if="position == 'e'"
        @submit="checkPosition('e')"
      />

      <FormulateForm
        v-model="values6"
        :schema="schemaF"
        class="
          mx-auto
          w-1/2 w-11/12
          max-w-md
          p-4
          mt-10
          rounded
          border-2 border-blue-200
        "
        v-if="position == 'f'"
        @submit="checkPosition('f')"
      />

      <FormulateForm
        v-model="values7"
        :schema="schemaG"
        class="
          mx-auto
          w-1/2 w-11/12
          max-w-md
          p-4
          mt-10
          rounded
          border-2 border-blue-200
        "
        v-if="position == 'g'"
        @submit="checkPosition('g')"
      />

      <FormulateForm
        v-model="values8"
        :schema="schemaH"
        class="
          mx-auto
          w-1/2 w-11/12
          max-w-md
          p-4
          mt-10
          rounded
          border-2 border-blue-200
        "
        v-if="position == 'h'"
        @submit="checkPosition('h')"
      />
    </div>
  </div>
  <div v-else>
    Thank you for your enrollment submission. We'll get back to you shortly.
  </div>
</template>

<script>
import schemaA from "~/assets/formSchema/enrollSchemaA.json";
import schemaB from "~/assets/formSchema/enrollSchemaB.json";
import schemaC from "~/assets/formSchema/enrollSchemaC.json";
import schemaD from "~/assets/formSchema/enrollSchemaD.json";
import schemaE from "~/assets/formSchema/enrollSchemaE.json";
import schemaF from "~/assets/formSchema/enrollSchemaF.json";
import schemaG from "~/assets/formSchema/enrollSchemaG.json";
import schemaH from "~/assets/formSchema/enrollSchemaH.json";

import FormAutoFill from "../node_modules/form-autofill/dist/globals/main.js"

export default {
  data() {
    return {
      values: {},
      values2: {},
      values3: {},
      values4: {},
      values5: {},
      values6: {},
      values7: {},
      values8: {},
      schemaA,
      schemaB,
      schemaC,
      schemaD,
      schemaE,
      schemaF,
      schemaG,
      schemaH,
      position: "",
      possiblePositions: ["a", "b", "c", "d", "e", "f", "g", "h"],
      error: "",
      success: "",
      applicationSelected: false,
      applicationSelectedType: "",
      applicationTypes: {
        extraLessons: ["a", "b", "c", "d", "e"],
        casualLearner: ["a", "b", "c", "d", "f"],
        supplementaryLearner: ["a", "b", "c", "d", "g"],
        extendedLearner: ["a", "b", "c", "d", "h"],
      },
    };
  },
  methods: {
    async submitForm() {
      let typeOfApplication = {
        name: "Type of Application",
        value: this.applicationSelectedType
      }
      let formInfo = {
        ...typeOfApplication,
        ...this.values,
        ...this.values2,
        ...this.values3,
        ...this.values4,
        ...this.values5,
        ...this.values6,
        ...this.values7,
        ...this.values8,
      };
      this.$axios.defaults.headers.post["Content-Type"] = "application/json";
      const submitForm = await this.$axios
        .post(
          "https://formsubmit.co/fe0534e16eb7e999e8d2461ce48f3360",
          formInfo
        )
        .then((res) =>
          res.status == 200
            ? (this.success = true)
            : (this.error = "There was a problem!")
        )
        .catch((e) => console.log(e));
    },
    applicationType(data) {
    FormAutoFill.fill()

      console.log(data);
      this.applicationSelected = true;
      this.applicationSelectedType = data;
      this.position = this.applicationTypes[data][0];
    },
    checkPosition(currentPos) {
    FormAutoFill.fill()

      let arrayToCheck = this.applicationTypes[this.applicationSelectedType];
      console.log(arrayToCheck);
      for (let i = 0; i <= arrayToCheck.length; i++) {
        if (arrayToCheck[i] == currentPos) {
          if (i == arrayToCheck.length - 1) {
            console.log("End position!");
            this.submitForm();
            return;
          }
          this.position = arrayToCheck[i + 1];
        }
      }
    },
  },
  mounted() {
    console.log(FormAutoFill.fill)
  }
};
</script>

<style>
.labels {
  @apply text-lg;
}

.inputs {
  @apply border-2 rounded pl-2 focus:border-blue-400 w-full text-base;
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
          text-center;
}
</style>