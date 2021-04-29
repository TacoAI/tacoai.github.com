<template>
    <v-container id="bottom-page" fluid class="d-flex">
    <v-row no-gutters class="align-self-start hideOnLandscape">
      <div class="bottom-page-top-cirlce">
          <!-- max-height="20vh" -->
        <v-img
          contain
          src="../assets/2-half-circle-down-black.png"
        ></v-img> 
      </div>
    </v-row>
  </v-container>

  <!--<v-container id="bottom-page" fluid>
    <v-row class="text-center">
      <v-col cols="6">
        <v-img
          :src="require('../assets/nlu-taco.png')"
          class="my-3"
          contain
          height="200"
        />
      </v-col>
       <v-col cols="6">
        <p>
          From building personalized user experiences to virtual assistants for back-office automation, TacoAI reduces scaling costs throughout the Prosperum ecosystem.
        </p>
        <p>
          Built on top of and extending Microsoft technologies, Taco AI provides a new client experience and connects data from multiple streams to unify the Prosperum back-office infrastructure.
        </p>
        <p>
          Taco AI is now building out chatbot systems for customer service, a revolutionary AI-powered trading experience, and creating an insights engine to glean connections between data.
        </p>
      </v-col>

       
    </v-row>
  </v-container>-->
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
  .bottom-page-top-cirlce{
    width: 100vw;
    max-width: 50vh;
    /* height: 12vw; */
    /* background: pink; */
    margin-right: auto;
    margin-left: auto;
  }

  @media (min-aspect-ratio: 2/3) {
    .hideOnLandscape {
        display: none;
    }
  }
  /* @media only screen and (orientation : portrait) { */
  @media (max-aspect-ratio: 2/3) {
    .hideOnPortrait {
        display: none;
    }
  }
</style>
