<template>
  <v-container fluid class="py-0">
    <v-row align="center" class="fill-height">
      <v-col md="3" sm="6" cols="12" class>
        <v-img
          :src="checkExistance(config.generalConfig.homeImage,0)?config.generalConfig.homeImage:require('@/assets/img/svg/iotLogo.png')"
          :lazy-src="checkExistance(config.generalConfig.homeImage,0)?config.generalConfig.homeImage:require('@/assets/img/svg/iot.png')"
          width="100%"
        >
          <template v-slot:placeholder>
            <v-row class="fill-height ma-0" align="center" justify="center">
              <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
            </v-row>
          </template>
        </v-img>
      </v-col>
      <v-col md="9" sm="6" cols="12" class="px-0">
        <p
          class="google-font mb-1"
          :class="$vuetify.theme.dark == true?'dark-font-color':'light-font-color'"
          style="font-weight: 350;font-size:230%"
        >
          <b>
            Internet de las cosas
            <span style="color: #1a73e8;">IoT</span>.
          </b>
        </p>
        <p class="google-font mt-0 mb-0" style="font-size:150%">Internet de las cosas en el hogar: un fenómeno imparable</p>
        <p class="google-font" style="font-size:100%">Nos guste o no, el internet de las cosas en el hogar ha llegado para quedarse. La tecnología es el futuro y sus aplicaciones más innovadoras pueden llegar a tu hogar mucho más rápido de lo que pueda parecer. Un ejemplo de ello es la tecnología de Internet de las Cosas – IoT (Internet of Things o, como se le denomina más recientemente, Internet of Everything), un concepto que se refiere a la interconexión digital de los objetos cotidianos con Internet, convirtiéndose así en objetos inteligentes.

 

Lo más atractivo de esta tecnología es que gracias a los aparatos conectados podemos mejorar nuestra calidad de vida, lograr establecer rutinas más sostenibles, alcanzar metas como la eficiencia energética o crear ecosistemas domésticos más confortables.</p>
        <p class="google-font" style="font-size:100%;color:#9e9e9e">
          
        </p>

        
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import { mapState } from "vuex";

export default {
  data: () => ({}),
  computed: {
    ...mapState(["config"])
  }
};
</script>

<style scoped>
.dark-font-color {
  color: white;
}
.light-font-color {
  color: #616161;
}
</style>