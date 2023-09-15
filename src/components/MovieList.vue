<script>
import axios from "axios";

export default {
  data() {
    return {
      title: "Lista dei film",
      characters: [],
    };
  },

  methods: {
    fetchCharacters() {
      axios
        .get(
          "https://api.themoviedb.org/3/search/movie?query=batman&api_key=6de6c3fec90304b52c1b139cc3f8055e"
        )
        .then((response) => {
          this.characters = response.data.results;
        });
    },
  },

  created() {
    this.fetchCharacters();
  },
};
</script>

<template>
  <h1>{{ title }}</h1>
  <div class="row">
    <div class="col" v-for="character in characters" :key="character.id">
      {{ character.name }}
    </div>
  </div>
</template>

<style lang="scss"></style>
