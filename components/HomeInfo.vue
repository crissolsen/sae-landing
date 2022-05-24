<template>
  <div class="w-11/12 mx-auto" id="about-us">
    <h1 class="text-center text-4xl mt-8">Sedgefield Academy of Excellence</h1>
    <h2 class="text-center text-xl">Self ~ Family ~ Community</h2>
    <div
      class="
        flex flex-columns
        py-6
        justify-evenly
        w-full
        md:w-3/4
        flex-wrap
        mx-auto
        text-lg
      "
    >
      <div class="card">
        <SpreadLove class="svg-image" />

        Sedgefield Academy of Excellence is a Home School Tutor Centre catering
        for learners from Grade R-12. We include GED, Cambridge, IMPAQ and Alpha
        support. We are dual medium, co-educational, affordable with
        Educators/Tutors who are eager to embrace a broad manner of tuition.
      </div>
      <div class="card">
        <Supports class="svg-image" />

        Small classes, where each child has quality time with their tutor,
        receiving focused, stimulating and exciting education. Independent
        learning is promoted while the teacher/tutor remains on hand to help
        with concepts the learners are struggling with. We offer support for
        learners with special educational needs. Learners are encouraged to
        practice self-discipline. SAE is not a school, but functions as a
        home-based Education Support Centre.
      </div>
      <div class="card">
        <Teaching class="svg-image" />

        SAE is a Centre that will be bringing about change in society by
        educating the learners about different aspects of everyday life and will
        not only be focusing on the basic curriculum. Learners will be taught
        values, morals, responsibility, self-love and self-acceptance as well as
        a variety of skills that are not available in other Centres/Schools.
      </div>
    </div>
  </div>
</template>

<script>
import SpreadLove from "~/assets/spreadLove.svg?inline";
import Supports from "~/assets/support.svg?inline";
import Teaching from "~/assets/teaching.svg?inline";

export default {
  components: {
    SpreadLove,
    Supports,
    Teaching,
  },
};
</script>

<style scoped>
.svg-image {
  @apply w-full max-h-52 pb-4;
}

.card {
  @apply max-w-xs border-8 rounded-xl p-4 my-2 border-blue-200 shadow-lg hover:shadow-2xl hover:border-blue-600 hover:-translate-y-3 transition transform;
}

</style>