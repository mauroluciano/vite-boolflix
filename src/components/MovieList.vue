<script>
import axios from "axios";

export default {
  data() {
    return {
      title: "Lista dei film",
      movies: [],
    };
  },

  methods: {
    fetchMovies() {
      axios
        .get(
          "https://api.themoviedb.org/3/search/movie?query=batman&api_key=6de6c3fec90304b52c1b139cc3f8055e"
        )
        .then((response) => {
          this.movies = response.data.results;
        });
    },
  },

  created() {
    this.fetchMovies();
  },
};
</script>

<template>
  <h1>{{ title }}</h1>
  <div class="row">
    <div class="col" v-for="movie in movies">
      {{ movie.name }}
    </div>
  </div>
</template>

<style lang="scss"></style>
