<script>
import axios from "axios";

export default {
  data() {
    return {
      title: "Lista dei film",
    };
  },

  created() {
    axios
      .get(
        "https://api.themoviedb.org/3/search/movie?query=batman&api_key=6de6c3fec90304b52c1b139cc3f8055e"
      )
      .then((res) => {
        console.log(res);
      });
  },
};
</script>

<template>
  <h1>{{ title }}</h1>
</template>

<style scoped></style>
