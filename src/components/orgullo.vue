<template>
  <div class="containerCred">
    <transition name="fade" mode="out-in">
      <v-form ref="form" v-if="value==0" key="1" class="height">
        <p
          class="text-center title mb-0"
        >Siento que mi participación es importante y que hace una diferencia en la organización</p>

        <v-chip-group
          v-model="orguIn42"
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
      <v-form ref="form" v-if="value==9" key="2" class="height">
        <p
          class="text-center title mb-0"
        >Mi trabajo tiene un significado especial para mí: éste no es “sólo un trabajo”</p>

        <v-chip-group
          v-model="orguIn43"
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
      <v-form ref="form" v-if="value==18" key="3" class="height">
        <p
          class="text-center title mb-0"
        >Cuando veo lo que logramos, me siento orgulloso</p>

        <v-chip-group
          v-model="orguEqui44"
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

      <v-form ref="form" v-if="value==27" key="4" class="height">
        <p
          class="text-center title mb-0"
        >Las personas están dispuestas a hacer un esfuerzo extra para hacer el trabajo</p>

        <v-chip-group
          v-model="orguEqui45"
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

      <v-form ref="form" v-if="value==36" key="5" class="height">
        <p class="text-center title mb-0">Las personas aquí se adaptan rápidamente a los cambios necesarios para el éxito de nuestra organización</p>

        <v-chip-group
          v-model="orguEqui46"
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

      <v-form ref="form" v-if="value==45" key="6" class="height">
        <p
          class="text-center title mb-0"
        >Quiero trabajar aquí por mucho tiempo</p>

        <v-chip-group
          v-model="orgImg47"
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

      <v-form ref="form" v-if="value==54" key="7" class="height">
        <p
          class="text-center title mb-0"
        >Estoy orgulloso de decir a otros que trabajo aquí</p>

        <v-chip-group
          v-model="orgImg48"
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

      <v-form ref="form" v-if="value==63" key="8" class="height">
        <p
          class="text-center title mb-0"
        >A las personas les gusta venir a trabajar</p>

        <v-chip-group
          v-model="orgImg49"
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
      <v-form ref="form" v-if="value==72" key="9" class="height">
        <p
          class="text-center title mb-0"
        >Me siento bien por la manera en que contribuimos como organización a la comunidad</p>

        <v-chip-group
          v-model="orgImg50"
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

      <v-form ref="form" v-if="value==81" key="10" class="height">
        <p
          class="text-center title mb-0"
        >Recomendaría a mis amigos y familiares trabajar en esta empresa por su excelente ambiente de trabajo</p>

        <v-chip-group
          v-model="orgImg51"
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

      <v-form ref="form" v-if="value==90" key="11" class="height">
        <p
          class="text-center title mb-0"
        >Nuestros clientes califican como excelente el servicio que les ofrecemos</p>

        <v-chip-group
          v-model="orgImg52"
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
        v-bind:disabled="orguIn42==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==9">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="orguIn43==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==18">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="orguEqui44==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>

    <div class="space-button" v-if="value==27">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="orguEqui45==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==36">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="orguEqui46==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>

    <div class="space-button" v-if="value==45">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="orgImg47==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==54">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="orgImg48==''"
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
        v-bind:disabled="orgImg49==''"
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
        v-bind:disabled="orgImg50==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==81">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="orgImg51==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==90">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="orgImg52==''"
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
  name: "orgullo",

  data: () => ({
    orguIn42: "",
    orguIn43: "",
    orguEqui44: "",
    orguEqui45: "",
    orguEqui46: "",
    orgImg47: "",
    orgImg48: "",
    orgImg49: "",
    orgImg50: "",
    orgImg51: "",
    orgImg52: "",

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
      if (this.value == 90) {
        // this.value = 100;
        // this.$emit("countProgress", this.value);
        this.orgImg52 = value;
        this.postCredibilidad();
        //firebase
      } else {
        let valor = this.value + 9;
        this.value = parseFloat(valor.toFixed(2));
        this.$emit("countProgress", this.value);
        // console.log(this.value);
      }
    },
    countUnprogress() {
      let valor = this.value - 9;
      this.value = parseFloat(valor.toFixed(2));
      this.$emit("countUnprogress", this.value);
      // console.log(this.value);
    },
    postCredibilidad() {
      this.value = 100;
      console.log(this.orgImg52);

      let orgullo = {
        orguIn42: this.orguIn42,
        orguIn43: this.orguIn43,
        orguEqui44: this.orguEqui44,
        orguEqui45: this.orguEqui45,
        orguEqui46: this.orguEqui46,
        orgImg47: this.orgImg47,
        orgImg48: this.orgImg48,
        orgImg49: this.orgImg49,
        orgImg50: this.orgImg50,
        orgImg51: this.orgImg51,
        orgImg52: this.orgImg52
      };
      let orgulloFull = JSON.parse(JSON.stringify(orgullo));
      // const ubicacionInicialKey = firebase
      //   .database()
      //   .ref("UBICACION_INICIAL")
      //   .push().key;

      firebase
        .database()
        .ref("ORGULLO")
        .child("ABCDE") //codigo
        .set(orgulloFull);

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

