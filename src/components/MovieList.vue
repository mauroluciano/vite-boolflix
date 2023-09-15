<script>
import { store } from "../data/store.js";
import SingleCard from "./SingleCard.vue";
export default {
  data() {
    return {
      store,
    };
  },
  components: { SingleCard },
};
</script>

<template>
  <div class="row">
    <div class="col">
      <SingleCard
        v-for="(movie, index) in store.movies"
        :key="index"
        :movie="movie" />
    </div>
  </div>
</template>

<style lang="scss"></style>
