<script>
import AppHeader from "./components/AppHeader.vue";
import MovieList from "./components/MovieList.vue";
import AppMain from "./components/AppMain.vue";
import { store } from "./data/store.js";
import axios from "axios";

export default {
  data() {
    return {
      title: "Lista dei film",
      store,
    };
  },

  components: { AppHeader, MovieList, AppMain },

  methods: {
    fetchMovies(term) {
      axios
        .get("https://api.themoviedb.org/3/search/movie", {
          params: {
            query: term,
            api_key: "6de6c3fec90304b52c1b139cc3f8055e",
          },
        })
        .then((response) => {
          this.store.movies = response.data.results;
        });
    },
  },

  created() {
    this.fetchMovies();
  },
};
</script>

<template>
  <AppHeader @start-search="fetchMovies" />
  <div class="container">
    <AppMain />
    <MovieList />
  </div>
</template>

<style lang="scss">
@use "./assets/styles/general.scss" as *;
</style>
