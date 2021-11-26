<template>
  <v-container fluid>
    <v-row align="center" justify="center">
      <v-col cols="12" md="3" lg="3" sm="4" class>
        <p class="google-font mb-0" style="font-size:150%">Una breve historia del IoT</p>
        <p
          class="google-font mt-0"
          style="font-size:95%"
        >El Internet de las cosas nació en 1982 con el primer dispositivo conectado de la historia: una máquina expendedora. Esta máquina inteligente empleaba sus capacidades para controlar las existencias e informar (los inventores podían conectarse para comprobar de forma remota si quedaban botellas de su refresco favorito, e incluso si estaban frías). Aunque la máquina expendedora inteligente no llegó a triunfar, sí predijo el uso a gran escala del IoT industrial, con fábricas que emplean sensores conectados para supervisar todos los aspectos de la cadena de suministro y los procesos de envío.

El nombre del invento, «Internet de las cosas», lo acuñó en 1999 el pionero de la tecnología Kevin Ashton.</p>
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