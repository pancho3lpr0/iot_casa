<template>
  <v-container fluid class="pa-0">
    <v-row align="center" class>
      <v-col cols="12" md="12" lg="12" sm="12" class="pa-0" style="color:white">
        <div class="ma-1">
          <div class="pa-5">
            <p class="google-font mb-0" style="font-size:150%">¿Cómo funciona realmente el Internet de las cosas?</p>
            <p
              class="google-font mt-0"
              style="font-size:95%"
            >Recuerde que el Internet de las cosas consiste en dispositivos ordinarios que pueden conectarse a Internet y comunicarse entre ellos a través de la nube. En general, eso significa añadir sensores especiales a objetos ordinarios como lavadoras, calefactores, neveras, relojes y prácticamente cualquier otra cosa.

Algunos dispositivos emplean estos sensores para recabar información y transmitirla. El primer dispositivo IoT que hemos mencionado antes, una máquina expendedora, utilizaba sensores para supervisar sus existencias y ponía esa información a disposición del propietario.

Otros dispositivos pueden recibir información y, a continuación, realizar una acción. Por ejemplo, una cerradura inteligente recibe de usted la señal de apertura y, en consecuencia, desbloquea una puerta.

Los dispositivos IoT más sofisticados (y más útiles, en general) pueden hacer ambas cosas. Un ejemplo del IoT industrial podría ser una fábrica que supervisa los componentes de la maquinaria en busca de posibles fallos y da la alarma cuando detecta un problema. En el IoT doméstico podría haber un termostato inteligente que recaba información sobre sus hábitos y preferencias de temperatura, para luego calentar o enfriar la casa según sus gustos para cada hora del día.

En general, la tecnología inteligente ayuda a las cosas a funcionar mejor, de forma más eficiente y sincronizada.

La mayoría de los artilugios IoT domésticos utilizan su router para conectarse al hogar inteligente, que le permite utilizar comandos de voz o el smartphone para controlar muchas funciones de la casa y así ahorrar tiempo, energía o ambas cosas.

Desde el punto de vista comercial, el IoT ayuda a las empresas a supervisar y gestionar fábricas, cadenas de suministro y muchas cosas más. También es posible añadir sensores a una parte dada de una gran maquinaria, como la perforadora de un pozo petrolífero, lo que ayuda a aumentar la producción y la seguridad.</p>
            <v-btn
              v-if="checkExistance(config.generalConfig.meetupLink,0)"
              :href="config.generalConfig.meetupLink"
              target="_blank"
              outlined
              color
              class="ma-0 google-font mb-2"
              style="border-radius:5px;text-transform: capitalize;color:white"
            >Meetup Page</v-btn>&nbsp;
            <br />
            <router-link
              to="/about"
              class="google-font"
              style="text-decoration:none;color:white"
            >See More about {{config.generalConfig.shortName || config.generalConfig.name}}</router-link>
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import { mapState } from "vuex";

export default {
  name: "App",
  data: () => ({}),
  computed: {
    ...mapState(["config"])
  }
};
</script>