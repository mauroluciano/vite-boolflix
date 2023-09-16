<script>
export default {
  data() {
    return {};
  },

  props: ["movie"],
};
</script>

<template>
  <div class="card" style="width: 18rem">
    <img :src="movie.poster_path" class="card-img-top" alt="..." />
    <div class="card-body">
      <h5 class="card-title">{{ movie.title }}</h5>
      <h1>{{ movie.original_title }}</h1>
      <p class="card-text">{{ movie.overview }}</p>
      <p>Release date: {{ movie.release_date }}</p>
      <p>Rate: {{ movie.vote_average }}</p>
      <p>Original language: {{ movie.original_language }}</p>
    </div>
  </div>
</template>

<style lang="scss"></style>
