<script>
import AppHeader from "./components/AppHeader.vue";
import MovieList from "./components/MovieList.vue";
import AppMain from "./components/AppMain.vue";
import { store } from "./data/store.js";
import axios from "axios";

export default {
  data() {
    return {
      store,
    };
  },

  components: { AppHeader, MovieList, AppMain },

  methods: {
    fetchMovies() {
      axios
        .get(
          "https://api.themoviedb.org/3/search/movie?query=batman&api_key=6de6c3fec90304b52c1b139cc3f8055e"
        )
        .then((response) => {
          store.movies = response.data.results;
          console.log(response.data.results);
        });
    },
  },

  created() {
    this.fetchMovies();
  },
};
</script>

<template>
  <AppHeader />
  <MovieList />
  <AppMain />
</template>

<style lang="scss">
@use "./assets/styles/general.scss";
</style>
