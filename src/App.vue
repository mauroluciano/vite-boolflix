<script setup>
import AppHeader from "./components/AppHeader.vue";
import MovieList from "./components/MovieList.vue";
import AppMain from "./components/AppMain.vue";
</script>

<template>
  <AppHeader />
  <MovieList />
  <AppMain />
</template>

<style lang="scss">
@use "./assets/styles/general.scss";
</style>
