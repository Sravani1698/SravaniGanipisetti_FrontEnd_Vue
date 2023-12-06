<template>
  <!--Step 3 use the component-->
  <MyHeader
    name="Marywood University"
    domains="marywood.edu"
    web_pages="http://www.marywood.edu"
    country="United States"
    alpha_two_code="US"
  />
  <UniversitiesList :universities=universities /> 
</template>

<script>
// Step: 1 Import the components
import MyHeader from "./components/MyHeader.vue";
import UniversitiesList from './components/UniversitiesList.vue'

export default {
  name: "App",

  // Step 2: Register the components
  components: {
    MyHeader,
    UniversitiesList
  },
  data() {
    return {
      universities: [],
    };
  },
  methods: {
    //promoises
    async fetchuniversities() {
     const res = await fetch(
        "https://sravani-ganipisetti-uq7x.onrender.com/api "
      );
      const data = await res.json();
      const universitiesData = data.universitiesList || [];
      console.log(data);
      return universitiesData;
    },
  },
  async created() {
    this.universities = await this.fetchuniversities();
  },

  // data() => this.data books
  // method => this.method => fetchbook
  // life cycle hooks created() => call our method here
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap");
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: "Montserrat", sans-serif;
}
.container {
  max-width: 400px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div {
  margin-bottom: 0.5em;
}
</style>
