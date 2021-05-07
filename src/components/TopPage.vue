<template>
  <v-container 
    id="top-page" 
    fluid>
    <v-row 
      no-gutters 
      class="hideOnLandscape">
      <v-spacer></v-spacer>
      <v-col 
        cols="7" 
        align-self="center">
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
      <v-col 
        :cols="aspectRatio > 2/3 ? '6': '12'"
        :class="aspectRatio >2/3 ? 'order-2' : 'order-1'"
        class="robo-taco-col">
        <div class="robot-taco-image">
        <v-img
          
          src="../assets/robot-taco-clear.png"/>
        </div>
      </v-col>
      <v-col 
        :cols="aspectRatio > 2/3 ? '6': '12'"
        :class="aspectRatio >2/3 ? 'order-1' : 'order-2'">
        <div 
          class="pitch d-flex align-content-space-around flex-wrap white--text"
          :class="aspectRatio >2/3 ? 'text-marging-onlandscape':'text-center'">
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
          <div class="hideOnPortrait">
            <v-btn
                :large="aspectRatio>2/3 ? true:false"
                class="text-capitalize body-text text-h6 font-weight-light grey darken-3 grey--text"
                href="mailto:info@prosperumholdings.com"
              >
                Contact Us
              </v-btn>
          </div>
        </div>
      </v-col>
    </v-row>
      <div class="top-page-bottom-circle">      
        <div class="contact-button hideOnLandscape">
          <v-btn
              :large="aspectRatio>2/3 ? true:false"
              class="text-capitalize body-text text-h6 font-weight-light black--text"
            >
              Contact Us
          </v-btn>
      </div>
        <v-img 
          src="../assets/2-half-circle-up-white.svg"/>
      </div>
  </v-container>
</template>

<script>
export default {
  name: "TopPage",
  props: {
    aspectRatio:{
      type: Number,
      required: true
    },
  }
};
</script>

<style scoped>
  .robo-taco-col{
    position: relative;
  }
  .side-logo{
    margin-top: 4vh;
  }
  .top-page-main{
    height: 80vh;
  }
  .top-page-up-circle {
    filter: invert(1);
  }
  #top-page {
    position: relative;
    background-color: black;
    height: 100vh;
    min-height: calc(100vw / 2.3);
    padding: 0px 0px;
  }
@media (min-aspect-ratio: 2/3) {
  .hideOnLandscape {
    display: none;
  }
  .text-marging-onlandscape{
    margin-left: 4vw;
    height: 75vh;
  }
  .robot-taco-image {
    position: absolute;
    width:90vh;
    max-width: 70vw;
    bottom: -1vh;
    right: -10vw;
  }
 .robot-taco-image .v-image{
    transform: rotate(0deg);
  }
  .main-title{
    font-size: 4.5vw;
    font-family:'Montserrat';
    line-height: 1.1;
    margin-bottom: 3vh;
    margin-top: calc(3vw*0.7);
  }
  .body-text{
    font-family:'Roboto';
    font-size: 2vw;
    line-height: 1.3
  }
  .top-page-bottom-circle .v-image{
    position: absolute;
    bottom: 0;
    width: 100vw;
    max-width:40vw;
    max-height:25vh;
  }
  .top-page-bottom-circle {
    position: absolute;
    z-index: 1;
    bottom: 0;
    left:40vw;
    height: 30vh;
    width:50vw
  }
}

@media (max-aspect-ratio: 2/3) {
  .hideOnPortrait {
    display: none;
  }
  .robot-taco-image{
    margin-top: 5vh;
    margin-left: 6vw;
    max-height: 48vh;
  }
  .robot-taco-image .v-image{
    transform: rotate(-20deg);
    width: 95vw;
    max-width: 53vh;
  }
  .pitch{
    margin-top:-13vh;
    margin-right: 30px;
    margin-left: 30px;
  }
  .main-title{
    font-size: 7vw;
    font-family:'Montserrat';
    line-height: 1.1;
    margin-bottom: 2vh;
  }
  .body-text{
    font-family:'Roboto';
    font-size: 4.5vw;
    line-height: 1.3
  }
  .top-page-bottom-circle .v-image{
    width: 90vw;
    max-width: 50vh;
    margin-right: auto;
    margin-left: auto;
  }
  .top-page-bottom-circle {
    position: absolute;
    z-index: 1;
    bottom: 0;
    width:100vw
  }
  .contact-button{
    z-index: 10;
    position: absolute;
    bottom: 0;
    width: 100vw; 
    display: flex;
    justify-content: center;
    align-items: center;
    height: 12vh;
  }
}
</style>