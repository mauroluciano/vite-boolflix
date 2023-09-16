<script>
import { store } from "../data/store.js";
import SingleCard from "./SingleCard.vue";
import AppMain from "./AppMain.vue";

export default {
  data() {
    return {
      store,
    };
  },
  components: { SingleCard, AppMain },
};
</script>

<template>
  <div class="row row-cols-4 d-flex">
    <SingleCard
      v-for="(movie, index) in store.movies"
      :key="index"
      :movie="store.movies[index]" />
  </div>
</template>

<style lang="scss"></style>
