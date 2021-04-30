<template>
  <v-container 
    fluid 
    id="bottom-page" 
    class="d-flex"
    :class="aspectRatio<2/3
      ?'flex-column justify-space-between'
      :'flex-column flex-wrap justify-center'">
    <div 
      class="bottom-page-top-cirlce hideOnLandscape">
      <v-img
        contain
        src="../assets/2-half-circle-down-black.png"
      ></v-img> 
    </div>
      <div
        class="body-text-bp "
        :class="aspectRatio<2/3
        ?'mt-2'
        :'order-2'">
        From building personalized user experiences to virtual assistants for back-office automation, TacoAI reduces scaling costs throughout the Prosperum ecosystem.
      </div>
      <div 
        class="bottom-page-taco-image"
        :class="aspectRatio<2/3
        ?''
        :'order-1 d-flex align-center'">
        <v-img
          src="../assets/singletaco.png"/>
      </div>  
      <div
        class="body-text-bp"
        :class="aspectRatio<2/3
        ?''
        :'order-3'">
        Built on top of and extending Microsoft technologies, Taco AI provides a new client experience and connects data from multiple streams to unify the Prosperum back-office infrastructure.
      </div>
      <div
        class="body-text-bp"
        :class="aspectRatio<2/3
          ?'mb-6'
          :'order-4'">
        Taco AI is now building out chatbot systems for customer service, a revolutionary AI-powered trading experience, and creating an insights engine to glean connections between data.
      </div>
  </v-container>
</template>

<script scoped>
  export default {
    name: 'BottomPage',
    props: {
      aspectRatio:{
        type: Number,
        required: true
      },
    }
  }
</script>

<style >
  #bottom-page{
    background-color: white;
    height: 100vh;
    min-height: calc(100vw/2.3);
    padding: 0px 0px;
  }

  /* orientation : landscape*/
  @media (min-aspect-ratio: 2/3) {
    .hideOnLandscape {
        display: none;
    }
    .body-text-bp{
      font-family:'Roboto';
      font-size: 2vw;
      line-height: 1.3;
      width:50vw;
      padding-left: 3vh;
      padding-right: 5vw;
      padding-top: 2vh;
      padding-bottom: 2vh;
    }
    .bottom-page-taco-image{
      min-width:50vw;
      height: 100vh;
    }
    .bottom-page-taco-image .v-image{
      width:50vw;
      max-width:100vh;
      margin-top: auto;
      margin-bottom: auto;
    }
  }
  /* orientation : portrait*/
  @media (max-aspect-ratio: 2/3) {
    .hideOnPortrait {
        display: none;
    }
    .bottom-page-top-cirlce{
      width: 100vw;
    }
    .bottom-page-top-cirlce .v-image{
      width:90vw;
      max-width:50vh;
      margin-right: auto;
      margin-left: auto;
    }
    .body-text-bp{
      font-family:'Roboto';
      font-size: 4vw;
      line-height: 2.6vh;
      margin-left: 5vw;
      margin-right: 5vw;
    }
    .bottom-page-taco-image{
      width:100vw
    }
    .bottom-page-taco-image .v-image{
      width:100vw;
      max-width:45vh;
      margin-right: auto;
      margin-left: auto;
    }
  }
</style>
