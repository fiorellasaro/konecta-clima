<template>
  <div class="container">
    <v-card class="mx-auto container" max-width="344">
      <h1 class="text-center mb-1 teal--text">ENCUESTA CLIMA KONECTA</h1>
      <v-img
        alt="Konecta weather"
        class="shrink margin-bottom"
        contain
        transition="scale-transition"
        src="../assets/weather.png"
        width="100"
      />
      <v-text-field
        color="teal"
        class="margin-bottom"
        v-model="code"
        :rules="codeRules"
        :counter="11"
        label="CÓDIGO"
        required
        v-on:input="messageStatus()"
      ></v-text-field>
      <v-btn
        class="white--text"
        x-large
        color="teal"
        v-bind:disabled="code.length<10"
        @click="validate()"
      >EMPEZAR</v-btn>
      <p v-if="messageState" class="feedback-message color-message">{{codeMessage}}</p>
      <p v-else class="message-blank color-message">{{codeMessage}}.</p>

    </v-card>
  </div>
</template>

<script>
import firebase from "firebase";

export default {
  name: "cardLogin",

  data: () => ({
    enterState: false,
    code: "",
    codes: {},
    codeFound: 0,
    codeMessage: "",
    messageState: false,
    codeRules: [
      v => !!v || "El código es requerido",
      v => v.length <= 11 || "El código debe ser de 10 u 11 caracteres"
    ]
  }),
  created() {
    this.codesData();
  },
  methods: {
    validate() {
      this.messageState = true;
      let state = this.codeState();
      console.log(state);
      if (state) {
        this.enterState = true;
        this.$emit("validate", this.enterState);
      } else {
        this.codeMessage = "El código no existe";
      }
    },
    codesData() {
      let codes = firebase.database().ref("CODIGOS");
      if (codes == undefined) {
        this.codeMessage = "El código no existe";
      } else {
        codes.on("value", this.getCodes, this.codigosErr);
      }
    },
    codeState() {
      for (let codigos in this.codes) {
        if (codigos == this.code) {
          if (codigos.state == undefined) {
            this.codeFound++;
            //this.codeMessage = "El código existe";
          } else {
            this.codeMessage = "El código ha sido usado";
          }
        }
      }
      if (this.codeFound > 0) {
        return true;
      } else {
        return false;
      }
    },
    getCodes(data) {
      this.codes = data.val();
    },
    codigosErr(err) {
      console.log("error");
      console.log(err);
    },
    messageStatus(){
      this.messageState = false;
    }
  }
};
</script>

<style >
.container {
  display: flex !important;
  justify-content: center !important;
  align-items: center !important;
  flex-direction: column !important;
}

.margin-bottom {
  margin-bottom: 1.5em;
}

.color-message {
  color: #ff5252 !important;
  font-size: 12px;
  margin-top: 0.5em;
}

.message-blank {
  visibility: hidden;
}
</style>

