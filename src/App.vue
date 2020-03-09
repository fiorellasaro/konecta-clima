<template>
  <v-app>
    <v-app-bar v-if="enterState"
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="./assets/k-blanco.png"
          transition="scale-transition"
          width="40"
        />


        <v-img
          alt="Konecta Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="./assets/konecta-b.png"
          width="100"
        />
      </div>
      <!-- <h2> - Clima</h2> -->
      <v-spacer></v-spacer>

    </v-app-bar>

    <v-content>
      <formClima v-if="enterState"></formClima>
      <cardLogin v-else v-on:validate="getEnterState($event)" />
    </v-content>
  </v-app>
</template>

<script>
import cardLogin from './components/cardLogin';
import formClima from './components/form';

export default {
  name: 'App',

  components: {
    cardLogin,
    formClima
  },

  data: () => ({
    enterState: false,
    //
  }),
  methods: {
    getEnterState(enter){
      this.enterState = enter;
    }
  }
};
</script>



