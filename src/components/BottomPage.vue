<template>
  <v-container>
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
  </v-container>
</template>

<script>
  export default {
    name: 'BottomPage',

    data: () => ({}),
  }
</script>
