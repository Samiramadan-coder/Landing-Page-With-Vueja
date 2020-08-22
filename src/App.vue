<!-- Template Tag -->
<template>
  <div id="app">

    <!-- Header Component -->
    <Header />

  </div>
</template>


<!-- JavaScript Tag -->
<script>

// Import The Header Component in the Parent Component
import Header from "./components/AppHeader.vue";

export default {
  name: 'App',
  components: {
    Header,
  },
  
};
</script>


<!-- Style Tag -->
<style>

  /* Global Style For All Elements */
  html, body{
    overflow: hidden;
  }

  /* CSS Variables */
  :root{
    --gray-color: #aba7a7;
    --main-color: #b1d234;
  }

</style>
