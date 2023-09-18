<script>
export default {
  data() {
    select: false;
  },

  methods: {
    showDiv() {
      this.select = true;
      console.log(this.select);
    },

    noShowDiv() {
      this.select = false;
      console.log(this.select);
    },
  },

  props: { movie: Object },
};
</script>

<template>
  <div class="col my-3">
    <div class="card" style="width: 18rem">
      <img
        :src="'https://image.tmdb.org/t/p/original' + movie.poster_path"
        class="card-img-top"
        alt="..." />

      <div class="card-body">
        <h5 class="card-title">{{ movie.title }}</h5>
        <h1>{{ movie.original_title }}</h1>
        <p class="card-text">{{ movie.overview }}</p>
        <p>Release date: {{ movie.release_date }}</p>
        <p>Rate: {{ movie.vote_average }}</p>
        <p>Original language: {{ movie.original_language }}</p>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.card-body {
  display: none;
  max-height: 430px;
  overflow-y: scroll;
}
.card:hover img {
  display: none;
}

.card:hover .card-body {
  display: initial !important;
}
</style>
