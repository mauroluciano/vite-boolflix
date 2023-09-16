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
      <a class="navbar-brand">BoolFlix </a>
      <form
        class="d-flex"
        role="search"
        @submit.prevent="$emit('start-search', term)">
        <input
          class="form-control me-2"
          type="search"
          v-model="term"
          placeholder="Search"
          aria-label="Search" />
        <button class="btn btn-outline-success" type="submit">Search</button>
      </form>
    </div>
  </nav>
</template>

<style lang="scss"></style>
