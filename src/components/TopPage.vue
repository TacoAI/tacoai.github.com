<template>
  <v-container fluid class="d-flex fill-height"  justify-content="space-between">  
    <v-row align="start" no-gutters justify="start">
      <v-col cols="7">
        <v-row>
          <v-col align-self="start">
            <svg width="297" height="109" viewBox="0 0 297 109" fill="none" xmlns="http://www.w3.org/2000/svg">
            <rect x="-73" width="370" height="109" rx="45" fill="white"/>
            <image x="55" y="-45" href="../assets/taco-logo.png" height="200" width="200"/>
            </svg>
          </v-col>
          <v-col align-self="start">
            <!-- <v-img
              fill-height
              contain
              max-width="677"
              src="../assets/bottom-math-circle-white.png"
            ></v-img> -->
          </v-col>
        </v-row>
        <v-row justify="center">
          <v-col align-self="center">
            <h1>
              Enhancing the Client and Professional Trading Experience
            </h1>
          </v-col>
        </v-row>
        <v-row>
          <v-col>
            <h3>
              Using cutting edge artifical intelligence and natural language processing, TacoAI builds tools for the FinTech revolution.
            </h3>
          </v-col>
        </v-row>
      </v-col>
       <v-col cols="5">
        <v-img
          contain
          width="100%"
          
          src="../assets/robot-taco-clear.png"
        ></v-img>
      </v-col>
     
    </v-row>
    <v-row class="text-center">
      <v-col cols="6">
        <v-img
          src="../assets/nlu-taco.png"
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

  </v-container>
</template>

<script>
  export default {
    name: 'TopPage',
    data: () => ({}),
  }
</script>

<style scoped>
  h1 {
    font-size: 86px;
    width: 90%;
    line-height: 1;
    /* margin: 0 !important; */
  }

  h3 {
    font-size: 42px;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    font-weight: lighter;
    line-height: 1;
  }
</style>