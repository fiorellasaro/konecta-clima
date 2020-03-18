<template>
  <div class="containerCred">
    <transition name="fade" mode="out-in">
      <v-form ref="form" v-if="value==0" key="1" class="height">
        <p
          class="text-center title mb-0"
        >A las personas aquí se les paga justamente por el trabajo que hacen</p>

        <v-chip-group
          v-model="imparEqui30"
          class="pt-6 chip-container"
          active-class="teal--text text--accent-4"
          :rules="[v => !!v || 'Selecciona una opción']"
        >
          <v-chip v-for="size in sizes" :key="size[0]" :value="size[0]" @click="countProgress">
            <v-icon color="#FFCA33" style="font-size: 35px;">{{size[1]}}</v-icon>
          </v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
      </v-form>
      <v-form ref="form" v-if="value==8" key="2" class="height">
        <p
          class="text-center title mb-0"
        >Siento que recibo una parte justa de las ganancias que obtiene esta organización</p>

        <v-chip-group
          v-model="imparEqui31"
          class="pt-6 chip-container"
          active-class="teal--text text--accent-4"
          :rules="[v => !!v || 'Selecciona una opción']"
          required
        >
          <v-chip v-for="size in sizes" :key="size[0]" :value="size[0]" @click="countProgress">
            <v-icon color="#FFCA33" style="font-size: 35px;">{{size[1]}}</v-icon>
          </v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
      </v-form>
      <v-form ref="form" v-if="value==16" key="3" class="height">
        <p
          class="text-center title mb-0"
        >Todos tenemos la oportunidad de recibir un reconocimiento especial</p>

        <v-chip-group
          v-model="imparEqui32"
          class="pt-6 chip-container"
          active-class="teal--text text--accent-4"
          :rules="[v => !!v || 'Selecciona una opción']"
          required
        >
          <v-chip v-for="size in sizes" :key="size[0]" :value="size[0]" @click="countProgress">
            <v-icon color="#FFCA33" style="font-size: 35px;">{{size[1]}}</v-icon>
          </v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
      </v-form>

      <v-form ref="form" v-if="value==24" key="4" class="height">
        <p
          class="text-center title mb-0"
        >Recibo un buen trato, independiente de mi posición en la organización</p>

        <v-chip-group
          v-model="imparEqui33"
          class="pt-6 chip-container"
          active-class="teal--text text--accent-4"
          :rules="[v => !!v || 'Selecciona una opción']"
          required
        >
          <v-chip v-for="size in sizes" :key="size[0]" :value="size[0]" @click="countProgress">
            <v-icon color="#FFCA33" style="font-size: 35px;">{{size[1]}}</v-icon>
          </v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
      </v-form>

      <v-form ref="form" v-if="value==32" key="5" class="height">
        <p
          class="text-center title mb-0"
        >Los ascensos se les da a quienes más se lo merecen</p>

        <v-chip-group
          v-model="imparAu34"
          class="pt-6 chip-container"
          active-class="teal--text text--accent-4"
          :rules="[v => !!v || 'Selecciona una opción']"
          required
        >
          <v-chip v-for="size in sizes" :key="size[0]" :value="size[0]" @click="countProgress">
            <v-icon color="#FFCA33" style="font-size: 35px;">{{size[1]}}</v-icon>
          </v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
      </v-form>

      <v-form ref="form" v-if="value==40" key="6" class="height">
        <p
          class="text-center title mb-0"
        >Los superiores inmediatos tratan a todos por igual; no hay favoritismos</p>

        <v-chip-group
          v-model="imparAu35"
          class="pt-6 chip-container"
          active-class="teal--text text--accent-4"
          :rules="[v => !!v || 'Selecciona una opción']"
          required
        >
          <v-chip v-for="size in sizes" :key="size[0]" :value="size[0]" @click="countProgress">
            <v-icon color="#FFCA33" style="font-size: 35px;">{{size[1]}}</v-icon>
          </v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
      </v-form>

      <v-form ref="form" v-if="value==48" key="7" class="height">
        <p
          class="text-center title mb-0"
        >Las personas evitan la manipulación, los rumores y "argollas" para conseguir sus objetivos</p>

        <v-chip-group
          v-model="imparAu36"
          class="pt-6 chip-container"
          active-class="teal--text text--accent-4"
          :rules="[v => !!v || 'Selecciona una opción']"
          required
        >
          <v-chip v-for="size in sizes" :key="size[0]" :value="size[0]" @click="countProgress">
            <v-icon color="#FFCA33" style="font-size: 35px;">{{size[1]}}</v-icon>
          </v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
      </v-form>

      <v-form ref="form" v-if="value==56" key="8" class="height">
        <p
          class="text-center title mb-0"
        >Las personas son tratadas de manera justa sin importar su edad</p>

        <v-chip-group
          v-model="imparTra37"
          class="pt-6 chip-container"
          active-class="teal--text text--accent-4"
          :rules="[v => !!v || 'Selecciona una opción']"
          required
        >
          <v-chip v-for="size in sizes" :key="size[0]" :value="size[0]" @click="countProgress">
            <v-icon color="#FFCA33" style="font-size: 35px;">{{size[1]}}</v-icon>
          </v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
      </v-form>
      <v-form ref="form" v-if="value==64" key="9" class="height">
        <p
          class="text-center title mb-0"
        >Las personas son tratadas de manera justa sin importar su condición socioeconómica</p>

        <v-chip-group
          v-model="imparTra38"
          class="pt-6 chip-container"
          active-class="teal--text text--accent-4"
          :rules="[v => !!v || 'Selecciona una opción']"
          required
        >
          <v-chip v-for="size in sizes" :key="size[0]" :value="size[0]" @click="countProgress">
            <v-icon color="#FFCA33" style="font-size: 35px;">{{size[1]}}</v-icon>
          </v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
      </v-form>

      <v-form ref="form" v-if="value==72" key="10" class="height">
        <p
          class="text-center title mb-0"
        >Las personas son tratadas de manera justa sin importar su género</p>

        <v-chip-group
          v-model="imparTra39"
          class="pt-6 chip-container"
          active-class="teal--text text--accent-4"
          :rules="[v => !!v || 'Selecciona una opción']"
          required
        >
          <v-chip v-for="size in sizes" :key="size[0]" :value="size[0]" @click="countProgress">
            <v-icon color="#FFCA33" style="font-size: 35px;">{{size[1]}}</v-icon>
          </v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
      </v-form>

      <v-form ref="form" v-if="value==80" key="11" class="height">
        <p class="text-center title mb-0">Las personas son tratadas de manera justa sin importar su orientación sexual</p>

        <v-chip-group
          v-model="imparTra40"
          class="pt-6 chip-container"
          active-class="teal--text text--accent-4"
          :rules="[v => !!v || 'Selecciona una opción']"
          required
        >
          <v-chip v-for="size in sizes" :key="size[0]" :value="size[0]" @click="countProgress">
            <v-icon color="#FFCA33" style="font-size: 35px;">{{size[1]}}</v-icon>
          </v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
      </v-form>

      <v-form ref="form" v-if="value==88" key="12" class="height">
        <p
          class="text-center title mb-0"
        >Si considero que se me ha tratado injustamente, sé que tendré la oportunidad de ser escuchado y que se me tratará con justicia</p>

        <v-chip-group
          v-model="imparTra41"
          class="pt-6 chip-container"
          active-class="teal--text text--accent-4"
          :rules="[v => !!v || 'Selecciona una opción']"
          required
        >
          <v-chip v-for="size in sizes" :key="size[0]" :value="size[0]" @click="countProgress(size[0])">
            <v-icon color="#FFCA33" style="font-size: 35px;">{{size[1]}}</v-icon>
          </v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
      </v-form>

      
    </transition>
    <div class="space-button" v-if="value==0">
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
        v-bind:disabled="imparEqui30==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==8">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="imparEqui31==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==16">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="imparEqui32==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>

    <div class="space-button" v-if="value==24">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="imparEqui33==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==32">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="imparAu34==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>

    <div class="space-button" v-if="value==40">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="imparAu35==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==48">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="imparAu36==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>

    <div class="space-button" v-if="value==56">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="imparTra37==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>

    <div class="space-button" v-if="value==64">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="imparTra38==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==72">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="imparTra39==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==80">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="imparTra40==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==88">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="imparTra41==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>

  </div>
</template>

<script>
import firebase from "firebase";

export default {
  name: "imparcialidad",

  data: () => ({
    imparEqui30: "",
    imparEqui31: "",
    imparEqui32: "",
    imparEqui33: "",
    imparAu34: "",
    imparAu35: "",
    imparAu36: "",
    imparTra37: "",
    imparTra38: "",
    imparTra39: "",
    imparTra40: "",
    imparTra41: "",

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
      if (this.value == 88) {
        // this.value = 100;
        // this.$emit("countProgress", this.value);
        this.imparTra41 = value;
        this.postImparcialidad();
        //firebase
      } else {
        let valor = this.value + 8;
        this.value = parseFloat(valor.toFixed(2));
        this.$emit("countProgress", this.value);
        // console.log(this.value);
      }
    },
    countUnprogress() {
      let valor = this.value - 8;
      this.value = parseFloat(valor.toFixed(2));
      this.$emit("countUnprogress", this.value);
      // console.log(this.value);
    },
    postImparcialidad() {
      this.value = 100;
      console.log(this.imparTra41);

      let imparcialidad = {
        imparEqui30: this.imparEqui30,
        imparEqui31: this.imparEqui31,
        imparEqui32: this.imparEqui32,
        imparEqui33: this.imparEqui33,
        imparAu34: this.imparAu34,
        imparAu35: this.imparAu35,
        imparAu36: this.imparAu36,
        imparTra37: this.imparTra37,
        imparTra38: this.imparTra38,
        imparTra39: this.imparTra39,
        imparTra40: this.imparTra40,
        imparTra41: this.imparTra41
      };
      let imparcialidadFull = JSON.parse(JSON.stringify(imparcialidad));
      // const ubicacionInicialKey = firebase
      //   .database()
      //   .ref("UBICACION_INICIAL")
      //   .push().key;

      firebase
        .database()
        .ref("IMPARCIALIDAD")
        .child("ABCDE") //codigo
        .set(imparcialidadFull);

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

