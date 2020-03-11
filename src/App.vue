<template>
  <v-app>
    <v-app-bar v-if="enterState" app color="teal" dark>
      <div class="d-flex align-center justify-content-center">
        <v-img
          alt="Konecta Name"
          class="shrink"
          contain
          transition="scale-transition"
          src="../src/assets/k-blanco.png"
          width="40"
        />
       <b color="white" class="m-0" style="font-size: 25px;">lima</b> 
      </div>
      <!-- <h2> - Clima</h2> -->
      <v-spacer></v-spacer>
    </v-app-bar>

    <v-content>
      <div class="container" v-if="enterState">
        <div class="progressContainer">
          <v-progress-linear
            :active="active"
            :background-opacity="opacity"
            :bottom="bottom"
            :buffer-value="buffer"
            :height="height"
            color="teal"
            style="border-radius: 100px;"
            :indeterminate="indeterminate"
            :query="query"
            :rounded="rounded"
            :stream="stream"
            :striped="striped"
            :top="top"
            :value="valueCredibilidad"
          ></v-progress-linear>
          <v-progress-linear
            :active="active"
            :background-opacity="opacity"
            :bottom="bottom"
            :buffer-value="buffer"
            :height="height"
            color="teal"
            style="border-radius: 100px;"
            :indeterminate="indeterminate"
            :query="query"
            :rounded="rounded"
            :stream="stream"
            :striped="striped"
            :top="top"
            :value="valueRespeto"
          ></v-progress-linear>
          <v-progress-linear
            :active="active"
            :background-opacity="opacity"
            :bottom="bottom"
            :buffer-value="buffer"
            :height="height"
            color="teal"
            style="border-radius: 100px;"
            :indeterminate="indeterminate"
            :query="query"
            :rounded="rounded"
            :stream="stream"
            :striped="striped"
            :top="top"
            :value="valueImparcialidad"
          ></v-progress-linear>
          <v-progress-linear
            :active="active"
            :background-opacity="opacity"
            :bottom="bottom"
            :buffer-value="buffer"
            :height="height"
            color="teal"
            style="border-radius: 100px;"
            :indeterminate="indeterminate"
            :query="query"
            :rounded="rounded"
            :stream="stream"
            :striped="striped"
            :top="top"
            :value="valueOrgullo"
          ></v-progress-linear>
          <v-progress-linear
            :active="active"
            :background-opacity="opacity"
            :bottom="bottom"
            :buffer-value="buffer"
            :height="height"
            color="teal"
            style="border-radius: 100px;"
            :indeterminate="indeterminate"
            :query="query"
            :rounded="rounded"
            :stream="stream"
            :striped="striped"
            :top="top"
            :value="valueCamaraderia"
          ></v-progress-linear>
        </div>

        <credibilidad
          v-on:countProgress="countCredibilidad($event)"
          v-on:countUnprogress="uncountCredibilidad($event)"
        ></credibilidad>
      </div>
      <cardLogin v-else v-on:validate="getEnterState($event)" />
    </v-content>
  </v-app>
</template>

<script>
import cardLogin from "./components/cardLogin";

import credibilidad from "./components/credibilidad";

export default {
  name: "App",

  components: {
    cardLogin,

    credibilidad
  },

  data: () => ({
    enterState: false,

    absolute: false,
    active: true,
    opacity: 0.3,
    bottom: false,
    buffer: 100,
    fixed: false,
    height: 20,
    indeterminate: false,
    query: false,
    rounded: false,
    stream: false,
    striped: false,
    top: false,
    valueCredibilidad: 0,

    valueRespeto: 0,
    valueImparcialidad: 0,
    valueOrgullo: 0,
    valueCamaraderia: 0
    //
  }),
  methods: {
    getEnterState(enter) {
      this.enterState = enter;
    },
    countCredibilidad(count) {
      this.valueCredibilidad = count;
      console.log(this.valueCredibilidad);
    },
    uncountCredibilidad(count) {
      this.valueCredibilidad = count;
      console.log(this.valueCredibilidad);
    }
  }
};
</script>


<style >
.container {
  width: 50% !important;
  display: flex;
  justify-content: center !important;
  align-items: center !important;
  flex-direction: column;
}

.progressContainer {
  width: 100% !important;
  display: flex;
  justify-content: space-between !important;
  align-items: center !important;
  flex-direction: row;
  margin-bottom: 1.5em;
  margin-top: 0.5em;
}

@media (max-width: 767px) {
  .container {
    width: 100% !important;
  }
}
</style>




