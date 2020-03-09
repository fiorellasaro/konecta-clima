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
    <v-form ref="form" v-if="value==0">
      <p
        class="text-center title mb-0"
      >Los superiores inmediatos me mantienen informado acerca de cosas y cambios importantes</p>

      <v-chip-group
        v-model="credibCom1"
        class="pt-6 chip-container"
        active-class="teal--text text--accent-4"
        :rules="[v => !!v || 'Selecciona una opción']"
        required
      >
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
      </v-chip-group>

      <v-row class="justify-space-between mx-3">
        <p class="body-2 pt-2 text-start" style="width: 75px">Nada de acuerdo</p>
        <p class="body-2 pt-2 text-end" style="width: 75px">Muy de acuerdo</p>
      </v-row>
      <div class="text-right">
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
    </v-form>
    <v-form ref="form" v-if="value==1.47">
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
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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
          v-bind:disabled="credibCom2==''"
          @click="countProgress"
        >
          <v-icon>mdi-arrow-right-bold</v-icon>
        </v-btn>
      </div>
    </v-form>

    <v-form ref="form" v-if="value==2.94">
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
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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
          v-bind:disabled="credibCom3==''"
          @click="countProgress"
        >
          <v-icon>mdi-arrow-right-bold</v-icon>
        </v-btn>
      </div>
    </v-form>

    <v-form ref="form" v-if="value==4.41">
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
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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
          v-bind:disabled="credibCom4==''"
          @click="countProgress"
        >
          <v-icon>mdi-arrow-right-bold</v-icon>
        </v-btn>
      </div>
    </v-form>

    <v-form ref="form" v-if="value==5.88">
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
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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
          v-bind:disabled="habGeren5==''"
          @click="countProgress"
        >
          <v-icon>mdi-arrow-right-bold</v-icon>
        </v-btn>
      </div>
    </v-form>

    <v-form ref="form" v-if="value==7.35">
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
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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
          v-bind:disabled="habGeren6==''"
          @click="countProgress"
        >
          <v-icon>mdi-arrow-right-bold</v-icon>
        </v-btn>
      </div>
    </v-form>

    <v-form ref="form" v-if="value==8.82">
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
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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
          v-bind:disabled="habGeren7==''"
          @click="countProgress"
        >
          <v-icon>mdi-arrow-right-bold</v-icon>
        </v-btn>
      </div>
    </v-form>

    <v-form ref="form" v-if="value==10.29">
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
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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
          v-bind:disabled="habGeren8==''"
          @click="countProgress"
        >
          <v-icon>mdi-arrow-right-bold</v-icon>
        </v-btn>
      </div>
    </v-form>
    <v-form ref="form" v-if="value==11.76">
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
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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
          v-bind:disabled="habGeren9==''"
          @click="countProgress"
        >
          <v-icon>mdi-arrow-right-bold</v-icon>
        </v-btn>
      </div>
    </v-form>

    <v-form ref="form" v-if="value==13.23">
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
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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
          v-bind:disabled="habGeren10==''"
          @click="countProgress"
        >
          <v-icon>mdi-arrow-right-bold</v-icon>
        </v-btn>
      </div>
    </v-form>

    <v-form ref="form" v-if="value==14.70">
      <p class="text-center title mb-0">Los superiores inmediatos cumplen sus promesas</p>

      <v-chip-group
        v-model="crediInte11"
        class="pt-6 chip-container"
        active-class="teal--text text--accent-4"
        :rules="[v => !!v || 'Selecciona una opción']"
        required
      >
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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
          v-bind:disabled="crediInte11==''"
          @click="countProgress"
        >
          <v-icon>mdi-arrow-right-bold</v-icon>
        </v-btn>
      </div>
    </v-form>

    <v-form ref="form" v-if="value==16.17">
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
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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
          v-bind:disabled="crediInte12==''"
          @click="countProgress"
        >
          <v-icon>mdi-arrow-right-bold</v-icon>
        </v-btn>
      </div>
    </v-form>

    <v-form ref="form" v-if="value==17.64">
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
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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
          v-bind:disabled="crediInte13==''"
          @click="countProgress"
        >
          <v-icon>mdi-arrow-right-bold</v-icon>
        </v-btn>
      </div>
    </v-form>

    <v-form ref="form" v-if="value==19.11">
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
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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
          v-bind:disabled="crediInte14==''"
          @click="countProgress"
        >
          <v-icon>mdi-arrow-right-bold</v-icon>
        </v-btn>
      </div>
    </v-form>

    <v-form ref="form" v-if="value==20.58">
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
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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
          v-bind:disabled="crediInte15==''"
          @click="countProgress"
        >
          <v-icon>mdi-arrow-right-bold</v-icon>
        </v-btn>
      </div>
    </v-form>

    <v-form ref="form" v-if="value==22.05">
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
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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
    <v-form ref="form" v-if="value==23.52">
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
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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

    <v-form ref="form" v-if="value==24.99">
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
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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

    <v-form ref="form" v-if="value==26.46">
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
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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

    <v-form ref="form" v-if="value==27.93">
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
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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
    <v-form ref="form" v-if="value==29.40">
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
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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

    <v-form ref="form" v-if="value==30.87">
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
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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

    <v-form ref="form" v-if="value==32.34">
      <p class="text-center title mb-0">Este es un lugar físicamente seguro donde trabajar</p>

      <v-chip-group
        v-model="resIn23"
        class="pt-6 chip-container"
        active-class="teal--text text--accent-4"
        :rules="[v => !!v || 'Selecciona una opción']"
        required
      >
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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
     <v-form ref="form" v-if="value==33.81">
      <p class="text-center title mb-0">Este es un lugar psicológica y emocionalmente saludable donde trabajar</p>

      <v-chip-group
        v-model="resIn24"
        class="pt-6 chip-container"
        active-class="teal--text text--accent-4"
        :rules="[v => !!v || 'Selecciona una opción']"
        required
      >
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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
    <v-form ref="form" v-if="value==35.28">
      <p class="text-center title mb-0">La infraestructura e instalaciones de la organización contribuyen a crear un buen ambiente de trabajo</p>

      <v-chip-group
        v-model="resIn25"
        class="pt-6 chip-container"
        active-class="teal--text text--accent-4"
        :rules="[v => !!v || 'Selecciona una opción']"
        required
      >
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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

    <v-form ref="form" v-if="value==36.75">
      <p class="text-center title mb-0">Puedo tomar tiempo libre, de forma coordinada, para atender asuntos personales de importancia</p>

      <v-chip-group
        v-model="resIn26"
        class="pt-6 chip-container"
        active-class="teal--text text--accent-4"
        :rules="[v => !!v || 'Selecciona una opción']"
        required
      >
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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

    <v-form ref="form" v-if="value==38.22">
      <p class="text-center title mb-0">Aquí se fomenta que las personas equilibren su vida de trabajo y su vida personal</p>

      <v-chip-group
        v-model="resIn27"
        class="pt-6 chip-container"
        active-class="teal--text text--accent-4"
        :rules="[v => !!v || 'Selecciona una opción']"
        required
      >
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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

    <v-form ref="form" v-if="value==39.69">
      <p class="text-center title mb-0">Los superiores inmediatos demuestran un interés sincero en mí como persona, no sólo como empleado</p>

      <v-chip-group
        v-model="resIn28"
        class="pt-6 chip-container"
        active-class="teal--text text--accent-4"
        :rules="[v => !!v || 'Selecciona una opción']"
        required
      >
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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

    <v-form ref="form" v-if="value==41.16">
      <p class="text-center title mb-0">Tenemos beneficios especiales y únicos en esta organización (no sólo económicos)</p>

      <v-chip-group
        v-model="resIn29"
        class="pt-6 chip-container"
        active-class="teal--text text--accent-4"
        :rules="[v => !!v || 'Selecciona una opción']"
        required
      >
        <v-chip v-for="size in sizes" :key="size" :value="size">{{ size }}</v-chip>
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

@media (max-width: 767px) {
  .container {
    width: 100% !important;
  }
}
</style>

