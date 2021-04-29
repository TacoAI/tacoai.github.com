<template>
  <v-container id="bottom-page" fluid>
    <div class="bottom-page-top-cirlce hideOnLandscape">
      <v-img
        contain
        src="../assets/2-half-circle-down-black.png"
      ></v-img> 
    </div>
    <v-row no-gutters>
        <div
          class="body-text mt-2">
          From building personalized user experiences to virtual assistants for back-office automation, TacoAI reduces scaling costs throughout the Prosperum ecosystem.
        </div>
        <div class="bottom-page-taco-image">
          <v-img
            src="../assets/singletaco.png"/>
        </div>  
        <div
          class="body-text">
          Built on top of and extending Microsoft technologies, Taco AI provides a new client experience and connects data from multiple streams to unify the Prosperum back-office infrastructure.
        </div>
        <div
          class="body-text mt-2">
          Taco AI is now building out chatbot systems for customer service, a revolutionary AI-powered trading experience, and creating an insights engine to glean connections between data.
        </div>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'BottomPage',

    data: () => ({}),
  }
</script>

<style >
  #bottom-page{
    background-color: white;
    height: 100vh;
    min-height: calc(100vw/2.3);
    padding: 0px 0px;
  }


  @media (min-aspect-ratio: 2/3) {
    .hideOnLandscape {
        display: none;
    }
      .body-text{
    font-family:'Roboto';
    font-size: calc(6vw*0.3);
    line-height: 1.3
  }
  }
  /* @media only screen and (orientation : portrait) { */
  @media (max-aspect-ratio: 2/3) {
    .hideOnPortrait {
        display: none;
    }
    .bottom-page-top-cirlce{
      width: 100vw;

    }
    .bottom-page-top-cirlce .v-image{
      width:100vw;
      max-width:50vh;
      margin-right: auto;
      margin-left: auto;
    }

    .body-text{
      font-family:'Roboto';
      font-size: 4vw;
      line-height: 2.4vh;
      margin-left: 4vw;
      margin-right: 4vw;
    }
    .bottom-page-taco-image{
      width:100vw
    }
    .bottom-page-taco-image .v-image{
      width:100vw;
      max-width:50vh;
      margin-right: auto;
      margin-left: auto;
    }
  }
</style>
