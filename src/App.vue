<template>
  <v-app id="app">
    <v-main>
      <TopPage/>
      <!-- <BottomPage/> -->
    </v-main>
  </v-app>
</template>

<script>
import TopPage from './components/TopPage';
// import BottomPage from './components/BottomPage';

export default {
  name: 'App',

  components: {
    TopPage,
    // BottomPage
  },

  data: () => ({
    //
  }),
};
</script>

<style scoped>
  /* #app {
    background-color: black;
  } */
</style>