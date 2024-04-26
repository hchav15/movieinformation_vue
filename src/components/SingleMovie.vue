<template>
  <div class="movie">
    <div class="movie-details">
      <img :src="movie.poster" width="250" height="300" alt="" />
      <h2 class="movie-name">{{ movie.name }}</h2>
      <div>
        <table>
          <tr>
            <th>Release year</th>
            <td>{{ movie.release_year }}</td>
          </tr>
          <tr>
            <th>Actors</th>
            <td>{{ movie.actors }}</td>
          </tr>
          <tr>
            <th>Director</th>
            <td>{{ movie.director }}</td>
          </tr>
          <tr>
            <th>Music Director</th>
            <td>{{ movie.music_director }}</td>
          </tr>
          <tr>
            <th>Rating</th>
            <td>{{ movie.rating }}</td>
          </tr>
          <tr>
            <th>Awards</th>
            <td>{{ movie.awards }}</td>
          </tr>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SingleMovie",
  props: {
    movie: Object,
  },
};
</script>

<style scoped>
.movie {
  margin-bottom: 0.5em;
}
.movie-details {
  margin: 0 15px;
  width: 350px;
  background-color: #fff;
  padding: 1.5em 1em;
}

.movie-name {
  margin: 20px 0;
}
@media screen and (max-width: 825px) {
  .movie-details {
    width: 250px;
    padding: 0;
  }
}
@media screen and (max-width: 625px) {
  .movie-details {
    width: 100%;
    padding: 1.5em 1em;
    margin: 0;
  }
}
</style>
