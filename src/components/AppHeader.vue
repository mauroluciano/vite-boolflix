<script>
export default {
  data() {
    return {
      term: "",
    };
  },
};
</script>

<template>
  <nav class="navbar bg-black">
    <div class="container-fluid">
      <a class="navbar-brand text-danger fs-4 fw-semibold">BoolFlix </a>
      <form
        class="d-flex"
        role="search"
        @submit.prevent="$emit('start-search', term)">
        <input
          class="form-control me-2"
          type="search"
          v-model="term"
          placeholder="Search your movie"
          aria-label="Search" />
        <button class="btn btn-outline-danger" type="submit">Search</button>
      </form>
    </div>
  </nav>
</template>

<style lang="scss"></style>
