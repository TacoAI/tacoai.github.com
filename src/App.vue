<template>
  <v-app id="app">
    <v-main>
      <!-- <TopPage/> -->
      <TopPage1/>
      <BottomPage/>
    </v-main>
  </v-app>
</template>

<script>
// import TopPage from './components/TopPage';
import TopPage1 from './components/TopPage1';
import BottomPage from './components/BottomPage';


export default {
  name: 'App',

  components: {
    // TopPage,
    TopPage1,
    BottomPage
  },

  data: () => ({
    //
  }),
};
</script>

<style>
  @import './styles/ress.css';
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@800&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@800&family=Roboto:wght@300&display=swap');
</style>