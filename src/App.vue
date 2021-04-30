<template>
  <v-app id="app">
    <v-main>
      <TopPage :aspectRatio="aspectRatio"/>
      <BottomPage :aspectRatio='aspectRatio'/>
    </v-main>
  </v-app>
</template>

<script>
import TopPage from './components/TopPage';
import BottomPage from './components/BottomPage';


export default {
  name: 'App',

  components: {
    TopPage,
    BottomPage
  },
  data: () => ({
    aspectRatio:0
  }),
  created() {
    window.addEventListener("resize", this.aspectRatioHandler);
  },
  destroyed() {
    window.removeEventListener("resize", this.aspectRatioHandler);
  },
  mounted() {
    this.aspectRatioHandler()
  },
  methods: {
    aspectRatioHandler () {
      this.aspectRatio = window.innerWidth / window.innerHeight
    }
  }

};
</script>

<style>
  @import './styles/ress.css';
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@800&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@800&family=Roboto:wght@300&display=swap');
</style>