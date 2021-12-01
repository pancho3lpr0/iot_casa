<template>
  <v-container fluid>
    <v-row align="center" justify="center">
      <v-col cols="12" md="3" lg="3" sm="4" class>
        <p class="google-font mb-0" style="font-size:150%">Tu hogar con IoT</p>
        <p
          class="google-font mt-0"
          style="font-size:95%"
        >un hogar inteligente permite vivir una vida màs sencilla y practica, ¿A quien no le gustaria poder controlar y gestionar en cualquier momento la iluminacion, los equipos audiovisuales, la temperatura de la calefaccion y el aire acondicionad o tu mascota, sin importar donde estas?</p>
        <p class="google-font" style="font-size:95%">About different Google technologies</p>
        <span v-for="(item,i) in whatwedodata" :key="i">
          <v-tooltip bottom>
            <template v-slot:activator="{ on }">
              <a :href="item.link" target="_blank" class="ma-0 mx-3" rel="noreferrer">
                <img :src="getImgUrl(item.image)" width="25vh" alt srcset dark v-on="on" />
              </a>
              &nbsp;&nbsp;&nbsp;
            </template>
            <span>{{item.TechName}}</span>
          </v-tooltip>
        </span>
      </v-col>
      <v-col cols="12" md="9" lg="9" sm="8">
        <v-container fluid>
          <v-row>
            <v-col md="3" lg="3" sm="6" cols="6" class="text-center pa-2">
              <v-icon large style="font-size:300%">mdi-comment</v-icon>
              <p class="google-font mt-2" style="font-size:130%"></p>
              <p
                class="google-font"
                style="font-size:95%"
              >RFID (identificación de radiofrecuencia) es un sistema de etiquetado que permite realizar un seguimiento de artículos o dispositivos y catalogarlos. Tradicionalmente se empleaba en el sector logístico (mediante chips) para hacer cosas como seguir contenedores alrededor del mundo o supervisar las piezas a medida que se desplazan por una línea de producción. Este seguimiento y supervisión a gran escala de dispositivos, piezas o cosas ayudó a tender los cimientos del IoT. De hecho, Ashton trabajaba en el RFID cuando acuñó el nombre del Internet de las cosas.</p>
            </v-col>
            <v-col md="3" lg="3" sm="6" cols="6" class="text-center pa-2">
              <v-icon large style="font-size:300%">mdi-code-tags</v-icon>
              <p class="google-font mt-2" style="font-size:130%"></p>
              <p
                class="google-font"
                style="font-size:95%"
              >La tecnología machine-to-machine (M2M), que toma el RFID y lo combina con la conectividad a Internet, permite a las máquinas conectarse, comunicarse entre ellas a través de una red y tomar decisiones sin interacción humana.</p>
            </v-col>
            <v-col md="3" lg="3" sm="6" cols="6" class="text-center pa-2">
              <v-icon large style="font-size:300%">mdi-school</v-icon>
              <p class="google-font mt-2" style="font-size:130%"></p>
              <p
                class="google-font"
                style="font-size:95%"
              >Otras tecnologías inalámbricas, unidas a la generalización del Internet de alta velocidad y unos costes de fabricación cada vez menores, crearon el escenario para el IoT.</p>
            </v-col>
            <v-col md="3" lg="3" sm="6" cols="6" class="text-center pa-2">
              <v-icon large style="font-size:300%">mdi-chart-bubble</v-icon>
              <p class="google-font mt-2" style="font-size:130%"></p>
              <p
                class="google-font"
                style="font-size:95%"
              >Para 2008, el Internet de las cosas ya había avanzado mucho. Fue en ese momento cuando Cisco comunicó que ya había más objetos que personas utilizando Internet.

La tecnología IoT tal vez tuviera unos principios modestos, pero ahora promete revolucionar la sociedad de incontables maneras, muchas de las cuales aún no podemos ni imaginar.</p>
            </v-col>
          </v-row>
        </v-container>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import whatwedodata from "@/assets/data/whatwedo.json";
export default {
  name: "App",
  data: () => ({
    whatwedodata: whatwedodata
  }),
  methods: {
    getImgUrl(url) {
      if (url.length > 0) {
        return require("@/assets/img/what-we-do/" + url);
      } else {
        return require("@/assets/img/what-we-do/notFound.png");
      }
    }
  }
};
</script>