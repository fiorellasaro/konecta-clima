<template>
   <div class="container">
    <h1>ENCUESTA CLIMA KONECTA</h1>
    <v-btn x-large color="success" dark @click="validate">EMPEZAR</v-btn>
   </div>

</template>

<script>
export default {
  name: "cardLogin",

  data: () => ({
      enterState: false,
  }),
  methods:{
      validate(){
          this.enterState=true;
          this.$emit("validate", this.enterState);
      }
  }
};
</script>

<style >
.container{
    display: flex;
    justify-content: center !important;
    align-items: center !important;
    flex-direction: column;

}
</style>

