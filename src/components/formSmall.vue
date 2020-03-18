<template>
  <div class="containerCred">
    <div v-for="question in questions" :key="question[0]">
      <transition-group name="fade" mode="out-in">
        <!-- <p v-if="show">hola</p> -->

        <v-form ref="form" v-if="value==question[1]" :key="`h ${question[0]}`" class="height">
          <p class="text-center title mb-0">{{question[2]}}</p>

          <v-chip-group
            v-model="credibilidad[question[0]-1]"
            class="pt-6 chip-container"
            active-class="teal--text text--accent-4"
            :rules="[v => !!v || 'Selecciona una opción']"
          >
            <v-chip
              v-for="size in sizes"
              :key="size[0]"
              :value="size[0]"
              @click="countProgress(size[0])"
            >
              <v-icon color="#FFCA33" style="font-size: 35px;">{{size[1]}}</v-icon>
            </v-chip>
          </v-chip-group>

          <v-row class="justify-space-between mx-3">
            <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
            <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
          </v-row>
        </v-form>
      </transition-group>

      <div class="space-button" v-if="value==question[1]">
        <v-btn
          class="white--text"
          fab
          light
          large
          color="#00B8AD"
          @click="countUnprogress"
          v-bind:disabled="value==0"
        >
          <v-icon>mdi-arrow-left-bold</v-icon>
        </v-btn>
        <v-btn
          class="white--text"
          fab
          light
          large
          color="#00B8AD"
          v-bind:disabled="credibilidad[question[0]-1]==''"
          @click="countProgress"
        >
          <v-icon>mdi-arrow-right-bold</v-icon>
        </v-btn>
      </div>
    </div>
  </div>
</template>

<script>
import firebase from "firebase";

export default {
  name: "credibilidad",

  data: () => ({
    credibilidad: ["", "", "", "", ""],
    questions: [
      [
        "1",
        0,
        "Los superiores inmediatos me mantienen informado acerca de cosas y cambios importantes"
      ],
      ["2", 6.5, "pregunta2"],
      ["3", 13, "pregunta3"],
      ["4", 19.5, "pregunta4"],
      ["5", 26, "pregunta5"]
    ],

    sizes: [
      ["1", "mdi-emoticon-cry-outline"],
      ["2", "mdi-emoticon-sad-outline"],
      ["3", "mdi-emoticon-neutral-outline"],
      ["4", "mdi-emoticon-happy-outline"],
      ["5", "mdi-emoticon-excited-outline"]
    ],
    value: 0
  }),
  methods: {
    countProgress(value) {
      //this.credibilidad.push(value);
      if (this.value == 26) {
        // this.value = 100;
        // this.$emit("countProgress", this.value);
        this.credibilidad[4] = value;
        this.postCredibilidad();
        //firebase
      } else {
        let valor = this.value + 6.5;
        this.value = parseFloat(valor.toFixed(2));
        this.$emit("countProgress", this.value);
        // console.log(this.value);
      }
    },
    countUnprogress() {
      let valor = this.value - 6.5;
      this.value = parseFloat(valor.toFixed(2));
      this.$emit("countUnprogress", this.value);
      // console.log(this.value);
    },
    postCredibilidad() {
      this.value = 100;
      // console.log(this.crediInte15);

      let credibilidadFull = JSON.parse(JSON.stringify(this.credibilidad));
      // const ubicacionInicialKey = firebase
      //   .database()
      //   .ref("UBICACION_INICIAL")
      //   .push().key;

      firebase
        .database()
        .ref("CREDIBILIDAD")
        .child("ABCDE") //codigo
        .set(credibilidadFull);

      this.$emit("countProgress", this.value);
    }
  }
};
</script>

<style >
.v-chip-group .v-slide-group__content {
  justify-content: space-between !important;
}
.v-chip-group .v-chip {
  margin: 0 !important;
}

.theme--light.v-chip:not(.v-chip--active) {
  background: white !important;
}
.height {
  height: 360px !important;
}
.containerCred {
  width: 100% !important;
  display: flex;
  justify-content: center !important;
  align-items: center !important;
  flex-direction: column;
}

.v-slide-group__content {
  display: flex !important;
  justify-content: space-around !important;
  align-items: center !important;
  flex-direction: row !important;
}

.space-button {
  width: 100%;
  display: flex !important;
  justify-content: space-between !important;
  align-items: center !important;
  flex-direction: row !important;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}

@media (max-width: 767px) {
  .container {
    width: 100% !important;
  }
}
</style>

