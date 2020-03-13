<template>
  <div class="containerCred">
    <transition name="fade" mode="out-in">
      <!-- <p v-if="show">hola</p> -->
      <v-form ref="form" v-if="value==0" key="1" class="height">
        <p
          class="text-center title mb-0"
        >Se me ofrece capacitación y/o entrenamiento con el objetivo de promover mi desarrollo profesional</p>

        <v-chip-group
          v-model="resApro16"
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
      <v-form ref="form" v-if="value==7" key="2" class="height">
        <p
          class="text-center title mb-0"
        >Me dan los recursos, herramientas y equipos para hacer mi trabajo</p>

        <v-chip-group
          v-model="resApro17"
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
      <v-form ref="form" v-if="value==14" key="3" class="height">
        <p
          class="text-center title mb-0"
        >Los superiores inmediatos muestran aprecio y reconocimiento por el buen trabajo y por el esfuerzo extra</p>

        <v-chip-group
          v-model="resApro18"
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

      <v-form ref="form" v-if="value==21" key="4" class="height">
        <p
          class="text-center title mb-0"
        >Los superiores inmediatos reconocen que pueden cometerse errores involuntarios en el trabajo</p>

        <v-chip-group
          v-model="resApro19"
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

      <v-form ref="form" v-if="value==28" key="5" class="height">
        <p
          class="text-center title mb-0"
        >Acá se reconoce a las personas que intentan nuevas y mejores maneras de hacer las cosas, independientemente del resultado</p>

        <v-chip-group
          v-model="resApro20"
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

      <v-form ref="form" v-if="value==35" key="6" class="height">
        <p
          class="text-center title mb-0"
        >Los superiores inmediatos incentivan, consideran y responden genuinamente a nuestras ideas y sugerencias</p>

        <v-chip-group
          v-model="resColab21"
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

      <v-form ref="form" v-if="value==42" key="7" class="height">
        <p
          class="text-center title mb-0"
        >Los superiores inmediatos involucran a las personas en decisiones relacionadas a su trabajo o a su ambiente de trabajo</p>

        <v-chip-group
          v-model="resColab22"
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

      <v-form ref="form" v-if="value==49" key="8" class="height">
        <p
          class="text-center title mb-0"
        >Este es un lugar físicamente seguro donde trabajar</p>

        <v-chip-group
          v-model="resIn23"
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
      <v-form ref="form" v-if="value==56" key="9" class="height">
        <p
          class="text-center title mb-0"
        >Este es un lugar psicológica y emocionalmente saludable donde trabajar</p>

        <v-chip-group
          v-model="resIn24"
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

      <v-form ref="form" v-if="value==63" key="10" class="height">
        <p
          class="text-center title mb-0"
        >La infraestructura e instalaciones de la organización contribuyen a crear un buen ambiente de trabajo</p>

        <v-chip-group
          v-model="resIn25"
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

      <v-form ref="form" v-if="value==70" key="11" class="height">
        <p class="text-center title mb-0">Puedo tomar tiempo libre, de forma coordinada, para atender asuntos personales de importancia</p>

        <v-chip-group
          v-model="resIn26"
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

      <v-form ref="form" v-if="value==77" key="12" class="height">
        <p
          class="text-center title mb-0"
        >Aquí se fomenta que las personas equilibren su vida de trabajo y su vida personal</p>

        <v-chip-group
          v-model="resIn27"
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

      <v-form ref="form" v-if="value==84" key="13" class="height">
        <p
          class="text-center title mb-0"
        >Los superiores inmediatos demuestran un interés sincero en mí como persona, no sólo como empleado</p>

        <v-chip-group
          v-model="resIn28"
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

      <v-form ref="form" v-if="value==91" key="14" class="height">
        <p
          class="text-center title mb-0"
        >Tenemos beneficios especiales y únicos en esta organización (no sólo económicos)</p>

        <v-chip-group
          v-model="resIn29"
          class="pt-6 chip-container"
          active-class="teal--text text--accent-4"
          :rules="[v => !!v || 'Selecciona una opción']"
          required
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
        v-bind:disabled="resApro16==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==7">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="resApro17==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==14">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="resApro18==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>

    <div class="space-button" v-if="value==21">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="resApro19==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==28">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="resApro20==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>

    <div class="space-button" v-if="value==35">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="resColab21==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==42">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="resColab22==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>

    <div class="space-button" v-if="value==49">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="resIn23==''"
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
        v-bind:disabled="resIn24==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==63">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="resIn25==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==70">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="resIn26==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==77">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="resIn27==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>

    <div class="space-button" v-if="value==84">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="resIn28==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>

    <div class="space-button" v-if="value==91">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="resIn29==''"
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
  name: "respeto",

  data: () => ({
    resApro16: "",
    resApro17: "",
    resApro18: "",
    resApro19: "",
    resApro20: "",
    resColab21: "",
    resColab22: "",
    resIn23: "",
    resIn24: "",
    resIn25: "",
    resIn26: "",
    resIn27: "",
    resIn28: "",
    resIn29: "",

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
      if (this.value == 91) {
        // this.value = 100;
        // this.$emit("countProgress", this.value);
        this.resIn29 = value;
        this.postRespeto();
        //firebase
      } else {
        let valor = this.value + 7;
        this.value = parseFloat(valor.toFixed(2));
        this.$emit("countProgress", this.value);
        // console.log(this.value);
      }
    },
    countUnprogress() {
      let valor = this.value - 7;
      this.value = parseFloat(valor.toFixed(2));
      this.$emit("countUnprogress", this.value);
      // console.log(this.value);
    },
    postRespeto() {
      this.value = 100;
      console.log(this.resIn29);

      let respeto = {
        resApro16: this.resApro16,
        resApro17: this.resApro17,
        resApro18: this.resApro18,
        resApro19: this.resApro19,
        resApro20: this.resApro20,
        resColab21: this.resColab21,
        resColab22: this.resColab22,
        resIn23: this.resIn23,
        resIn24: this.resIn24,
        resIn25: this.resIn25,
        resIn26: this.resIn26,
        resIn27: this.resIn27,
        resIn28: this.resIn28,
        resIn29: this.resIn29
      };

      let respetoFull = JSON.parse(JSON.stringify(respeto));
      // const ubicacionInicialKey = firebase
      //   .database()
      //   .ref("UBICACION_INICIAL")
      //   .push().key;

      firebase
        .database()
        .ref("RESPETO")
        .child("ABCDE") //codigo
        .set(respetoFull);

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

