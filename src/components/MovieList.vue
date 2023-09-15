<script></script>

<template>
  <h1>{{ title }}</h1>
  <div class="row">
    <div class="col">
      <ul>
        <li :v-for="movie in movies" :key="movie.id">{{ movie.title }}</li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss"></style>
