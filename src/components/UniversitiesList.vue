<template>
  <div v-for="university of universities" :key="university.name">
    <SingleUniversity :university="university" />
  </div>
</template>
<script>
import SingleUniversity from "./SingleUniversity.vue";

export default {
  name: "UniversitiesList",
  props: {
    universities: Array,
  },
  components: {
    SingleUniversity,
  },
};
</script>
<style scoped></style>
