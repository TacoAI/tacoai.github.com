<template>
  <v-container id="top-page" fluid>
    <v-row no-gutters class="hideOnLandscape">
      <v-spacer></v-spacer>
      <v-col cols="7" align-self="center">
        <div>
          <v-img src="../assets/tacoAiTopLogo.svg" />
        </div>
      </v-col>
      <v-spacer></v-spacer>
    </v-row>
    <v-row no-gutters class="hideOnPortrait">
      <v-col
        cols="3"
        align-self="start">
        <v-img
          class="side-logo"
          position="start" 
          contain
          max-height="10vh"          
          src="../assets/tacoAiSideLogo.svg"/>
      </v-col>
      <v-col>
          <v-img
            class="top-page-up-circle ml-8"
            position="start"
            contain
            max-width="45vw"
            max-height="25vh"
            src="../assets/2-half-circle-down-black.svg" />
      </v-col>
    </v-row>
    <v-row no-gutters class="top-page-main mt-n8">
        <!-- :class="{'custom2cols': aspectRatio > 2/3}"  -->
      <v-col 
        :cols="aspectRatio > 2/3 ? '6': '12'"
        :class="aspectRatio >2/3 ? 'order-2' : 'order-1'"
        class="white--text">
        <v-img
          class="robot-taco-image"
          src="../assets/robot-taco-clear.png"/>
      </v-col>
        <!-- :class="{'custom2cols': aspectRatio > 2/3}"  -->
      <v-col 
        :cols="aspectRatio > 2/3 ? '6': '12'"
        :class="aspectRatio >2/3 ? 'order-1' : 'order-2'">
        <div 
          class="d-flex align-content-space-around flex-wrap white--text"
          :class="aspectRatio >2/3 ? 'text-marging-onlandscape':'text-center mx-14'">
          <div>
            <div 
              class="main-title">
              Building Tools for the FinTech Revolution
            </div>
            <div 
              class="body-text">
              Using cutting edge artificial intelligence and natural language
              processing, TacoAI creates a unique client and professional trading
              experience.
            </div>
          </div>
          <div>
            <v-btn
                :large="aspectRatio>2/3 ? true:false"
                class="text-capitalize body-text text-h6 font-weight-light grey darken-3 grey--text"
              >
                Contact Us
              </v-btn>
          </div>
        </div>
      </v-col>
    </v-row>
    <!-- <v-row no-gutters>
      <v-col style="background:gray"> -->
      <div class="top-page-bottom-circle">
        <v-img 
          contain
          max-width="40vw"
          max-height="25vh"
          src="../assets/2-half-circle-up-white.svg"></v-img>
      </div>
      <!-- </v-col>
    </v-row> -->
  </v-container>
</template>

<script>
// import TacoLogoPortrait from "./icons/TacoLogoPortrait"
// import TacoLogoMathPortrait from "./icons/TacoLogoMathPortrait"
export default {
  name: "TopPage",
  components: {
    // TacoLogoPortrait,
    // TacoLogoMathPortrait,
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

<style scoped>
.side-logo{
  margin-top: 4vh;
}
.top-page-main{
  height: 80vh;
}
.text-marging-onlandscape{
  margin-left: 4vw;
  height: 75vh;
}
.main-title{
  font-size: 5vw;
  font-family:'Montserrat';
  line-height: 1.1;
  margin-bottom: 3vh;
  margin-top: calc(0.3vh*7);
}
.body-text{
  font-family:'Roboto';
  font-size: 2vw;
  line-height: 1.3
}
.robot-taco-image {
  transform: rotate(-28deg);
  position: absolute;
  width:90vh;
  max-width: 70vw;
  bottom: -2vh;
  right: -10vw;
  /* background-color: grey;
  max-height: 90vh; */
}
.top-page-up-circle {
  filter: invert(1);
}
.top-page-bottom-circle .v-image{
  /* height: 30vh; */
  position: absolute;
  bottom: 0;
  width: 100vw;
}
.top-page-bottom-circle {
  position: absolute;
  /* display: block; */
  z-index: 1;
  bottom: 0;
  left:40vw;
  height: 30vh;
  /* background: blue; */
  /* height: 20vh; */
  width:50vw
  /* max-width: 50vh; */
  /* height: 12vw; */
  /* background: pink; */
  /* margin-right: auto;
  margin-left: auto; */
}
/* .btn-contact-us{
    position: absolute;
    z-index: 9999;
    width:100%;
    height:100%;
  } */
#top-page {
  position: relative;
  background-color: black;
  height: 100vh;
  min-height: calc(100vw / 2.3);
  padding: 0px 0px;
}
/* .bottom-image-container{
    max-height: 250px;
    margin-left: auto;
    margin-right: auto;
    width: 100vw
  } */
/* h1 {
    font-size: 86px;
    width: 90%;
    line-height: 1; */
/* margin: 0 !important; */
/* } */

/* h3 {
    font-size: 42px;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    font-weight: lighter;
    line-height: 1;
    left: 20vw;  } */
/* @media only screen and (min-device-width : 768px) and (orientation : landscape) { */
@media (min-aspect-ratio: 2/3) {
  .hideOnLandscape {
    display: none;
  }
  /* .top-page-bottom-circle {
    width: 50vw;
    max-width: 50vh;
    margin-left: 40vw;
    margin-right: auto;
  } */
  .robot-taco-image {
    transform: rotate(-0deg);
  }
  /* .custom2cols {
    width: 50%;
    max-width: 50%;
    flex-basis: 50%;
  } */
}
/* @media only screen and (orientation : portrait) { */
@media (max-aspect-ratio: 2/3) {
  .hideOnPortrait {
    display: none;
  }
  .robot-taco-image{
    position: relative;
  }
  .top-page-bottom-circle {
  position: absolute;
  /* display: block; */
  z-index: 1;
  bottom: 0;
  left:40vw;
  height: 30vh;
  /* background: blue; */
  /* height: 20vh; */
  width:50vw;
  /* max-width: 50vh; */
  /* height: 12vw; */
  /* background: pink; */
  /* margin-right: auto;
  margin-left: auto; */
    width: 100vw;
    max-width: 50vh;
}
}
</style>