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
        <div v-if="valueCamaraderia!=100" class="progressContainer">
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
        <div v-else class="align-final">
          <h1 class="text-center">¡Gracias por participar!</h1>
        <v-img
          alt="Konecta Name"
          class="shrink"
          contain
          transition="scale-transition"
          src="../src/assets/weather.png"
          width="200"
        />

        </div>

        <credibilidad
          v-if="valueCredibilidad!=100"
          v-on:countProgress="countCredibilidad($event)"
          v-on:countUnprogress="uncountCredibilidad($event)"
        ></credibilidad>
        <!-- <formSmall
          v-if="valueCredibilidad!=100"
          v-on:countProgress="countCredibilidad($event)"
          v-on:countUnprogress="uncountCredibilidad($event)"
        ></formSmall>-->
        <respeto
          v-else-if="valueRespeto!=100"
          v-on:countProgress="countRespeto($event)"
          v-on:countUnprogress="uncountRespeto($event)"
        ></respeto>
        <imparcialidad
          v-else-if="valueImparcialidad!=100"
          v-on:countProgress="countImparcialidad($event)"
          v-on:countUnprogress="uncountImparcialidad($event)"
        ></imparcialidad>
        <orgullo
          v-else-if="valueOrgullo!=100"
          v-on:countProgress="countOrgullo($event)"
          v-on:countUnprogress="uncountOrgullo($event)"
        ></orgullo>
        <camaraderiaPlus
          v-else-if="valueCamaraderia!=100"
          v-on:countProgress="countCamaraderiaPlus($event)"
          v-on:countUnprogress="uncountCamaraderiaPlus($event)"
        ></camaraderiaPlus>
      </div>
      <cardLogin v-else v-on:validate="getEnterState($event)" />
    </v-content>
  </v-app>
</template>

<script>
import cardLogin from "./components/cardLogin";

import credibilidad from "./components/credibilidad";
import respeto from "./components/respeto";
import imparcialidad from "./components/imparcialidad";
import orgullo from "./components/orgullo";
import camaraderiaPlus from "./components/camaraderiaPlus";
// import formSmall from "./components/formSmall";

export default {
  name: "App",

  components: {
    cardLogin,
    // formSmall,

    credibilidad,
    respeto,
    imparcialidad,
    orgullo,
    camaraderiaPlus
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
    },
    countRespeto(count) {
      this.valueRespeto = count;
      console.log(this.valueRespeto);
    },
    uncountRespeto(count) {
      this.valueRespeto = count;
      console.log(this.valueRespeto);
    },
    countImparcialidad(count) {
      this.valueImparcialidad = count;
      console.log(this.valueImparcialidad);
    },
    uncountImparcialidad(count) {
      this.valueImparcialidad = count;
      console.log(this.valueImparcialidad);
    },
    countOrgullo(count) {
      this.valueOrgullo = count;
      console.log(this.valueOrgullo);
    },
    uncountOrgullo(count) {
      this.valueOrgullo = count;
      console.log(this.valueOrgullo);
    },
    countCamaraderiaPlus(count) {
      this.valueCamaraderia = count;
      console.log(this.valueCamaraderia);
    },
    uncountCamaraderiaPlus(count) {
      this.valueCamaraderia = count;
      console.log(this.valueCamaraderia);
    }
  }
};
</script>


<style >
.v-progress-linear {
  width: 19% !important;
}
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

.align-final{
  display:flex;
  align-items: center !important;
  flex-direction: column;
}

@media (max-width: 767px) {
  .container {
    width: 100% !important;
  }
}
</style>




