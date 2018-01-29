<template>
  <div>
      <p>hi from {{ name }}</p>
      <nuxt-link to="/">Home page</nuxt-link>
  </div>
</template>

<script>
export default {
 layout:'main',
  data({ req }) {
    return {
      name: req ? "server" : "client"
    };
  },

};
</script>

