<template>
  <div class="containerCred">
    <!-- <v-progress-linear
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
    ></v-progress-linear> -->
    <transition name="fade" mode="out-in">
      <!-- <p v-if="show">hola</p> -->
      <v-form ref="form" v-if="value==0" key="1" class="height">
        <p
          class="text-center title mb-0"
        >Los superiores inmediatos me mantienen informado acerca de cosas y cambios importantes</p>

        <v-chip-group
          v-model="credibCom1"
          class="pt-6 chip-container"
          active-class="teal--text text--accent-4"
          :rules="[v => !!v || 'Selecciona una opción']"
        >
          <v-chip v-for="size in sizes" :key="size" :value="size" @click="countProgress">{{ size }}</v-chip>
        </v-chip-group>

        <v-row class="justify-space-between mx-3">
          <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
          <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
        </v-row>
      </v-form>
      <v-form ref="form" v-if="value==6.5" key="2" class="height">
        <p
          class="text-center title mb-0"
        >Los superiores inmediatos comunican claramente qué se espera de nuestro trabajo</p>

        <v-chip-group
          v-model="credibCom2"
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
      </v-form>
      <v-form ref="form" v-if="value==13" key="3" class="height">
        <p
          class="text-center title mb-0"
        >Puedo hacer cualquier pregunta razonable a los superiores inmediatos y recibir una respuesta directa</p>

        <v-chip-group
          v-model="credibCom3"
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
      </v-form>

      <v-form ref="form" v-if="value==19.5" key="4" class="height">
        <p
          class="text-center title mb-0"
        >Los superiores inmediatos son accesibles, es fácil hablar con ellos</p>

        <v-chip-group
          v-model="credibCom4"
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
      </v-form>

      <v-form ref="form" v-if="value==26" key="5" class="height">
        <p
          class="text-center title mb-0"
        >Los superiores inmediatos son competentes en el manejo del negocio</p>

        <v-chip-group
          v-model="habGeren5"
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
      </v-form>

      <v-form ref="form" v-if="value==32.5" key="6" class="height">
        <p
          class="text-center title mb-0"
        >Los superiores inmediatos hacen un buen trabajo en la asignación de labores y coordinación de las personas</p>

        <v-chip-group
          v-model="habGeren6"
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
      </v-form>

      <v-form ref="form" v-if="value==39" key="7" class="height">
        <p
          class="text-center title mb-0"
        >Las personas que ingresan a la organización encajan bien con nuestra cultura</p>

        <v-chip-group
          v-model="habGeren7"
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
      </v-form>

      <v-form ref="form" v-if="value==45.5" key="8" class="height">
        <p
          class="text-center title mb-0"
        >Los superiores inmediatos confían en que las personas harán un buen trabajo sin tener que estar supervisándolos</p>

        <v-chip-group
          v-model="habGeren8"
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
      </v-form>
      <v-form ref="form" v-if="value==52" key="9" class="height">
        <p
          class="text-center title mb-0"
        >Las personas son responsables de cumplir con su trabajo adecuadamente</p>

        <v-chip-group
          v-model="habGeren9"
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
      </v-form>

      <v-form ref="form" v-if="value==58.5" key="10" class="height">
        <p
          class="text-center title mb-0"
        >Los superiores inmediatos tienen una visión clara de hacia dónde va la organización y qué hacer para lograrlo</p>

        <v-chip-group
          v-model="habGeren10"
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
      </v-form>

      <v-form ref="form" v-if="value==65" key="11" class="height">
        <p class="text-center title mb-0">Los superiores inmediatos cumplen sus promesas</p>

        <v-chip-group
          v-model="crediInte11"
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
      </v-form>

      <v-form ref="form" v-if="value==71.5" key="12" class="height">
        <p
          class="text-center title mb-0"
        >Las palabras de los superiores inmediatos coinciden con sus acciones</p>

        <v-chip-group
          v-model="crediInte12"
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
      </v-form>

      <v-form ref="form" v-if="value==78" key="13" class="height">
        <p
          class="text-center title mb-0"
        >Creo que aquí se haría todo lo posible antes de tener que hacer una reducción de personal</p>

        <v-chip-group
          v-model="crediInte13"
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
      </v-form>

      <v-form ref="form" v-if="value==84.5" key="14" class="height">
        <p
          class="text-center title mb-0"
        >Nuestros ejecutivos representan plenamente los valores de nuestra organización</p>

        <v-chip-group
          v-model="crediInte14"
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
      </v-form>

      <v-form ref="form" v-if="value==91" key="15" class="height">
        <p
          class="text-center title mb-0"
        >Los superiores inmediatos conducen el negocio de manera ética y honesta</p>

        <v-chip-group
          v-model="crediInte15"
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
        v-bind:disabled="credibCom1==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==6.5">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="credibCom2==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==13">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="credibCom3==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>

    <div class="space-button" v-if="value==19.5">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="credibCom4==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==26">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="habGeren5==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>

    <div class="space-button" v-if="value==32.5">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="habGeren6==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==39">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="habGeren7==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>

    <div class="space-button" v-if="value==45.5">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="habGeren8==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>

    <div class="space-button" v-if="value==52">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="habGeren9==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==58.5">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="habGeren10==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==65">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="crediInte11==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==71.5">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="crediInte12==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>

    <div class="space-button" v-if="value==78">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="crediInte13==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>

    <div class="space-button" v-if="value==84.5">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="crediInte14==''"
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
        v-bind:disabled="crediInte15==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
  </div>
</template>

<script>
export default {
  name: "credibilidad",

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

    sizes: ["1", "2", "3", "4", "5"],

    // absolute: false,
    // active: true,
    // opacity: 0.3,
    // bottom: false,
    // buffer: 100,
    // fixed: false,
    // height: 20,
    // indeterminate: false,
    // query: false,
    // rounded: false,
    // stream: false,
    // striped: false,
    // top: false,
    value: 0
  }),
  methods: {
    countProgress() {
      if (this.value == 91) {
        this.value = 100;
        this.$emit("countProgress", this.value);
        console.log(this.value + "hola");
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
    }
  }
};
</script>

<style >
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

