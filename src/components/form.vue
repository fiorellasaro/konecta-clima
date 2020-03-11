<template>
  <div class="container">
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
      :value="value"
    ></v-progress-linear>
    <transition name="fade" mode="out-in">
     
      <v-form ref="form" v-if="value==22.05" key="16">
        <p
          class="text-center title mb-0"
        >Se me ofrece capacitación y/o entrenamiento con el objetivo de promover mi desarrollo profesional</p>

        <v-chip-group
          v-model="resApo16"
          class="pt-6 chip-container"
          active-class="teal--text text--accent-4"
          :rules="[v => !!v || 'Selecciona una opción']"
          required
        >
          <v-chip v-for="size in sizes" :key="size" :value="size" @click="countProgress">{{ size }}</v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
        <div class="space-button">
          <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
            <v-icon>mdi-arrow-left-bold</v-icon>
          </v-btn>
          <v-btn
            class="white--text"
            fab
            light
            large
            color="#00B8AD"
            v-bind:disabled="resApo16==''"
            @click="countProgress"
          >
            <v-icon>mdi-arrow-right-bold</v-icon>
          </v-btn>
        </div>
      </v-form>
      <v-form ref="form" v-if="value==23.52" key="17">
        <p
          class="text-center title mb-0"
        >Me dan los recursos, herramientas y equipos para hacer mi trabajo</p>

        <v-chip-group
          v-model="resApo17"
          class="pt-6 chip-container"
          active-class="teal--text text--accent-4"
          :rules="[v => !!v || 'Selecciona una opción']"
          required
        >
          <v-chip v-for="size in sizes" :key="size" :value="size" @click="countProgress">{{ size }}</v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
        <div class="space-button">
          <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
            <v-icon>mdi-arrow-left-bold</v-icon>
          </v-btn>
          <v-btn
            class="white--text"
            fab
            light
            large
            color="#00B8AD"
            v-bind:disabled="resApo17==''"
            @click="countProgress"
          >
            <v-icon>mdi-arrow-right-bold</v-icon>
          </v-btn>
        </div>
      </v-form>

      <v-form ref="form" v-if="value==24.99" key="18">
        <p
          class="text-center title mb-0"
        >Los superiores inmediatos muestran aprecio y reconocimiento por el buen trabajo y por el esfuerzo extra</p>

        <v-chip-group
          v-model="resApo18"
          class="pt-6 chip-container"
          active-class="teal--text text--accent-4"
          :rules="[v => !!v || 'Selecciona una opción']"
          required
        >
          <v-chip v-for="size in sizes" :key="size" :value="size" @click="countProgress">{{ size }}</v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
        <div class="space-button">
          <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
            <v-icon>mdi-arrow-left-bold</v-icon>
          </v-btn>
          <v-btn
            class="white--text"
            fab
            light
            large
            color="#00B8AD"
            v-bind:disabled="resApo18==''"
            @click="countProgress"
          >
            <v-icon>mdi-arrow-right-bold</v-icon>
          </v-btn>
        </div>
      </v-form>

      <v-form ref="form" v-if="value==26.46" key="19">
        <p
          class="text-center title mb-0"
        >Los superiores inmediatos reconocen que pueden cometerse errores involuntarios en el trabajo</p>

        <v-chip-group
          v-model="resApo19"
          class="pt-6 chip-container"
          active-class="teal--text text--accent-4"
          :rules="[v => !!v || 'Selecciona una opción']"
          required
        >
          <v-chip v-for="size in sizes" :key="size" :value="size" @click="countProgress">{{ size }}</v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
        <div class="space-button">
          <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
            <v-icon>mdi-arrow-left-bold</v-icon>
          </v-btn>
          <v-btn
            class="white--text"
            fab
            light
            large
            color="#00B8AD"
            v-bind:disabled="resApo19==''"
            @click="countProgress"
          >
            <v-icon>mdi-arrow-right-bold</v-icon>
          </v-btn>
        </div>
      </v-form>

      <v-form ref="form" v-if="value==27.93" key="20">
        <p
          class="text-center title mb-0"
        >Acá se reconoce a las personas que intentan nuevas y mejores maneras de hacer las cosas, independientemente del resultado</p>

        <v-chip-group
          v-model="resApo20"
          class="pt-6 chip-container"
          active-class="teal--text text--accent-4"
          :rules="[v => !!v || 'Selecciona una opción']"
          required
        >
          <v-chip v-for="size in sizes" :key="size" :value="size" @click="countProgress">{{ size }}</v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
        <div class="space-button">
          <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
            <v-icon>mdi-arrow-left-bold</v-icon>
          </v-btn>
          <v-btn
            class="white--text"
            fab
            light
            large
            color="#00B8AD"
            v-bind:disabled="resApo20==''"
            @click="countProgress"
          >
            <v-icon>mdi-arrow-right-bold</v-icon>
          </v-btn>
        </div>
      </v-form>
      <v-form ref="form" v-if="value==29.40" key="21">
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
          <v-chip v-for="size in sizes" :key="size" :value="size" @click="countProgress">{{ size }}</v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
        <div class="space-button">
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
      </v-form>

      <v-form ref="form" v-if="value==30.87" key="22">
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
          <v-chip v-for="size in sizes" :key="size" :value="size" @click="countProgress">{{ size }}</v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
        <div class="space-button">
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
      </v-form>

      <v-form ref="form" v-if="value==32.34" key="23">
        <p class="text-center title mb-0">Este es un lugar físicamente seguro donde trabajar</p>

        <v-chip-group
          v-model="resIn23"
          class="pt-6 chip-container"
          active-class="teal--text text--accent-4"
          :rules="[v => !!v || 'Selecciona una opción']"
          required
        >
          <v-chip v-for="size in sizes" :key="size" :value="size" @click="countProgress">{{ size }}</v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
        <div class="space-button">
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
      </v-form>
      <v-form ref="form" v-if="value==33.81" key="24">
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
          <v-chip v-for="size in sizes" :key="size" :value="size" @click="countProgress">{{ size }}</v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
        <div class="space-button">
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
      </v-form>
      <v-form ref="form" v-if="value==35.28" key="25">
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
          <v-chip v-for="size in sizes" :key="size" :value="size" @click="countProgress">{{ size }}</v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
        <div class="space-button">
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
      </v-form>

      <v-form ref="form" v-if="value==36.75" key="26">
        <p
          class="text-center title mb-0"
        >Puedo tomar tiempo libre, de forma coordinada, para atender asuntos personales de importancia</p>

        <v-chip-group
          v-model="resIn26"
          class="pt-6 chip-container"
          active-class="teal--text text--accent-4"
          :rules="[v => !!v || 'Selecciona una opción']"
          required
        >
          <v-chip v-for="size in sizes" :key="size" :value="size" @click="countProgress">{{ size }}</v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
        <div class="space-button">
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
      </v-form>

      <v-form ref="form" v-if="value==38.22" key="27">
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
          <v-chip v-for="size in sizes" :key="size" :value="size" @click="countProgress">{{ size }}</v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
        <div class="space-button">
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
      </v-form>

      <v-form ref="form" v-if="value==39.69" key="28">
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
          <v-chip v-for="size in sizes" :key="size" :value="size" @click="countProgress">{{ size }}</v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
        <div class="space-button">
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
      </v-form>

      <v-form ref="form" v-if="value==41.16" key="29">
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
          <v-chip v-for="size in sizes" :key="size" :value="size" @click="countProgress">{{ size }}</v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
        <div class="space-button">
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
      </v-form>
    </transition>
  </div>
</template>

<script>
export default {
  name: "formClima",
  

  data: () => ({
    first: "",
    second: "",

    credibCom1: "",
    credibCom2: "",
    credibCom3: "",
    credibCom4: "",
    habGeren5: "",
    habGeren6: "",
    habGeren7: "",
    habGeren8: "",
    habGeren9: "",
    habGeren10: "",
    crediInte11: "",
    crediInte12: "",
    crediInte13: "",
    crediInte14: "",
    crediInte15: "",
    resApo16: "",
    resApo17: "",
    resApo18: "",
    resApo19: "",
    resApo20: "",
    resColab21: "",
    resColab22: "",
    resIn23: "",
    resIn24: "",
    resIn25: "",
    resIn26: "",
    resIn27: "",
    resIn28: "",
    resIn29: "",
    sizes: ["1", "2", "3", "4", "5"],

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
    value: 0
  }),
  methods: {
    countProgress() {
      let valor = this.value + 1.47;
      this.value = parseFloat(valor.toFixed(2));
      console.log(this.value);
    },
    countUnprogress() {
      let valor = this.value - 1.47;
      this.value = parseFloat(valor.toFixed(2));
      console.log(this.value);
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

.v-slide-group__content {
  display: flex !important;
  justify-content: space-around !important;
  align-items: center !important;
  flex-direction: row !important;
}

.space-button {
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

