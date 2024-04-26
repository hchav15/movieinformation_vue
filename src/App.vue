<template>
  <div class="movies-container">
    <MyHeader appName="Movie Information" />
    <AllMovies :movies="movies" />
  </div>
</template>

<script>
import AllMovies from "./components/AllMovies.vue";
import MyHeader from "./components/MyHeader.vue";

export default {
  name: "App",

  components: {
    MyHeader,
    AllMovies,
  },
  data() {
    return {
      movies: [],
    };
  },
  methods: {
    async getMovies() {
      const res = await fetch("https://movieinformation-node.onrender.com/api");
      const data = await res.json();

      return data.movies;
    },
  },
  async created() {
    this.movies = await this.getMovies();
  },
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

.movies-container {
  background-color: darkgray;
  color: black;
  padding: 1em;
  text-align: center;
}
</style>
