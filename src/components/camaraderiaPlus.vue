<template>
  <div class="containerCred">
    <transition name="fade" mode="out-in">
      <v-form ref="form" v-if="value==0" key="1" class="height">
        <p class="text-center title mb-0">Puedo ser yo mismo en mi lugar de trabajo</p>

        <v-chip-group
          v-model="camFam53"
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
      <v-form ref="form" v-if="value==6" key="2" class="height">
        <p class="text-center title mb-0">Aquí se celebran eventos especiales</p>

        <v-chip-group
          v-model="camFam54"
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
      <v-form ref="form" v-if="value==12" key="3" class="height">
        <p class="text-center title mb-0">Las personas aquí se preocupan por sus compañeros</p>

        <v-chip-group
          v-model="camFam55"
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

      <v-form ref="form" v-if="value==18" key="4" class="height">
        <p class="text-center title mb-0">Este es un lugar entretenido donde trabajar</p>

        <v-chip-group
          v-model="camHos56"
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

      <v-form ref="form" v-if="value==24" key="5" class="height">
        <p
          class="text-center title mb-0"
        >Cuando ingresas a la organización se te hace sentir bienvenido</p>

        <v-chip-group
          v-model="camHos57"
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

      <v-form ref="form" v-if="value==30" key="6" class="height">
        <p
          class="text-center title mb-0"
        >Cuando las personas cambian de función o de área de trabajo, se les hace sentir como en casa</p>

        <v-chip-group
          v-model="camHos58"
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

      <v-form ref="form" v-if="value==36" key="7" class="height">
        <p class="text-center title mb-0">Uno puede contar con la colaboración de las personas</p>

        <v-chip-group
          v-model="camSen59"
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

      <v-form ref="form" v-if="value==42" key="8" class="height">
        <p
          class="text-center title mb-0"
        >Tomando todo en consideración, yo diría que este es un gran lugar donde trabajar</p>

        <v-chip-group
          v-model="camGestalt60"
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
      <v-form ref="form" v-if="value==48" key="9" class="height">
        <p
          class="text-center title mb-0"
        >Recibiste alguna presión o incentivo de parte de tus superiores inmediatos u otras áreas de tu empresa para contestar de cierta forma a la encuesta</p>

        <v-chip-group
          v-model="pAdicional61"
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

      <v-form ref="form" v-if="value==54" key="10" class="height">
        <p
          class="text-center title mb-0"
        >La organización realiza esfuerzos por reducir su impacto en el medio ambiente</p>

        <v-chip-group
          v-model="pNacional62"
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

      <v-form ref="form" v-if="value==60" key="11" class="height">
        <p
          class="text-center title mb-0"
        >Acá me dan oportunidades de crecer profesionalmente y hacer línea de carrera.</p>

        <v-chip-group
          v-model="pNacional63"
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

      <v-form ref="form" v-if="value==66" key="12" class="height">
        <p
          class="text-center title mb-0"
        >Recomendaría los productos y servicios de esta organización a mis conocidos</p>

        <v-chip-group
          v-model="pNacional64"
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
      <v-form ref="form" v-if="value==72" key="13" class="height">
        <p
          class="text-center title mb-0"
        >Aquí me dan oportunidades de participar en actividades que benefician a la comunidad</p>

        <v-chip-group
          v-model="pNacional65"
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
      <v-form ref="form" v-if="value==78" key="14" class="height">
        <p class="text-center title mb-0">Considero que mi desempeño es evaluado de manera justa</p>

        <v-chip-group
          v-model="pNacional66"
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
      <v-form ref="form" v-if="value==84" key="15" class="height">
        <p
          class="text-center title mb-0"
        >La comunicación entre áreas facilita el logro de los objetivos</p>

        <v-chip-group
          v-model="pNacional67"
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
      <v-form ref="form" v-if="value==90" key="16" class="height">
        <p
          class="text-center title mb-0"
        >Conozco mis objetivos y cómo mi trabajo contribuye a los resultados del negocio</p>

        <v-chip-group
          v-model="pNacional68"
          class="pt-6 chip-container"
          active-class="teal--text text--accent-4"
          :rules="[v => !!v || 'Selecciona una opción']"
          required
        >
          <v-chip v-for="size in sizes" :key="size[0]" :value="size[0]">
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
        v-bind:disabled="camFam53==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==6">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="camFam54==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==12">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="camFam55==''"
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
        v-bind:disabled="camHos56==''"
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
        v-bind:disabled="camHos57==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>

    <div class="space-button" v-if="value==30">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="camHos58==''"
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
        v-bind:disabled="camSen59==''"
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
        v-bind:disabled="camGestalt60==''"
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
        v-bind:disabled="pAdicional61==''"
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
        v-bind:disabled="pNacional62==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==60">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="pNacional63==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==66">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="pNacional64==''"
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
        v-bind:disabled="pNacional65==''"
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
        v-bind:disabled="pNacional66==''"
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
        v-bind:disabled="pNacional67==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>
    </div>
    <div class="space-button" v-if="value==90">
      <v-btn class="white--text" fab light large color="#00B8AD" @click="countUnprogress">
        <v-icon>mdi-arrow-left-bold</v-icon>
      </v-btn>
      <!-- <v-btn
        class="white--text"
        fab
        light
        large
        color="#00B8AD"
        v-bind:disabled="pNacional68==''"
        @click="countProgress"
      >
        <v-icon>mdi-arrow-right-bold</v-icon>
      </v-btn>-->
      <v-btn
        x-large
        color="teal"
        class="white--text"
        v-bind:disabled="pNacional68==''"
        @click="countProgress"
      >FINALIZAR</v-btn>
    </div>
  </div>
</template>

<script>
import firebase from "firebase";

export default {
  name: "camaraderiaPlus",

  data: () => ({
    camFam53: "",
    camFam54: "",
    camFam55: "",
    camHos56: "",
    camHos57: "",
    camHos58: "",
    camSen59: "",
    camGestalt60: "",
    pAdicional61: "",
    pNacional62: "",
    pNacional63: "",
    pNacional64: "",
    pNacional65: "",
    pNacional66: "",
    pNacional67: "",
    pNacional68: "",

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
    countProgress() {
      if (this.value == 90) {
        // this.value = 100;
        // this.$emit("countProgress", this.value);
       // this.pNacional68 = value;
        this.postCamaraderiaPlus();
        //firebase
      } else {
        let valor = this.value + 6;
        this.value = parseFloat(valor.toFixed(2));
        this.$emit("countProgress", this.value);
        // console.log(this.value);
      }
    },
    countUnprogress() {
      let valor = this.value - 6;
      this.value = parseFloat(valor.toFixed(2));
      this.$emit("countUnprogress", this.value);
      // console.log(this.value);
    },
    postCamaraderiaPlus() {
      this.value = 100;
     // console.log(this.pNacional68);

      let camaraderia = {
        camFam53: this.camFam53,
        camFam54: this.camFam54,
        camFam55: this.camFam55,
        camHos56: this.camHos56,
        camHos57: this.camHos57,
        camHos58: this.camHos58,
        camSen59: this.camSen59,
        camGestalt60: this.camGestalt60
      };
      let camaraderiaFull = JSON.parse(JSON.stringify(camaraderia));

      firebase
        .database()
        .ref("CAMARADERIA")
        .child("ABCDE") //codigo
        .set(camaraderiaFull);

      let pNacionales = {
        pAdicional61: this.pAdicional61,
        pNacional62: this.pNacional62,
        pNacional63: this.pNacional63,
        pNacional64: this.pNacional64,
        pNacional65: this.pNacional65,
        pNacional66: this.pNacional66,
        pNacional67: this.pNacional67,
        pNacional68: this.pNacional68
      };

      let pNacionalesFull = JSON.parse(JSON.stringify(pNacionales));

      firebase
        .database()
        .ref("P_NACIONALES")
        .child("ABCDE") //codigo
        .set(pNacionalesFull);

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

