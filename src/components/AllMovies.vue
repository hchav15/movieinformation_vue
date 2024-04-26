<template>
  <div class="movies">
    <div v-for="movie of movies" :key="movie.id">
      <SingleMovie :movie="movie" />
    </div>
  </div>
</template>
<script>
import SingleMovie from "./SingleMovie.vue";

export default {
  name: "AllMovies",
  props: {
    movies: Array,
  },
  components: {
    SingleMovie,
  },
};
</script>
<style scoped>
.movies {
  display: flex;
  flex-wrap: wrap;
  width: 100%;
  justify-content: space-between;
}
@media screen and (max-width: 625px) {
  movies {
    flex-direction: column;
  }
}
</style>
