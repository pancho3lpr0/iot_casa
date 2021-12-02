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
              <v-icon large style="font-size:300%">mdi-wifi</v-icon>
              <p class="google-font mt-2" style="font-size:130%">Conectividad, La clave de IoT</p>
              <p
                class="google-font"
                style="font-size:95%"
              >Internet de las cosas (Internet of Things) consiste en conectar objetos gracias a la tecnologia y en crear una nueva relaciòn entre ellos. El internet de todo (Internet of Everything) va mas alla. En este se incluyen la relacion entre objetos, pero tambien entre ellos y las propias personas. La informacion y los datos son esenciales, pero avamzamos hacia la interaccion de los propios
              </p>
            </v-col>
            <v-col md="3" lg="3" sm="6" cols="6" class="text-center pa-2">
              <v-icon large style="font-size:300%">mdi-battery</v-icon>
              <p class="google-font mt-2" style="font-size:130%">Ahorro</p>
              <p
                class="google-font"
                style="font-size:95%"
              >Con un sistema energetico conectado en el hogar los consumidores pueden ahorrar entorno a un 20% al mes</p>
            </v-col>
            <v-col md="3" lg="3" sm="6" cols="6" class="text-center pa-2">
              <v-icon large style="font-size:300%">mdi-security</v-icon>
              <p class="google-font mt-2" style="font-size:130%">Seguridad</p>
              <p
                class="google-font"
                style="font-size:95%"
              >IoT permite mejorar la seguridad del hogar con sistemas de acceso con huella digital, las alertas automatizadas y las camaras conectadas...</p>
            </v-col>
            <v-col md="3" lg="3" sm="6" cols="6" class="text-center pa-2">
              <v-icon large style="font-size:300%" >mdi-comment</v-icon>
              <p class="google-font mt-2" style="font-size:130%">Intercambio de informacion</p>
              <p
                class="google-font"
                style="font-size:95%"
              >Los aparatos conectados intercambian informacion de forma constante entre ellos para generar un "estilo de vida" propio en nuestro hogar conectado. Las maquinas conocen nuestros habitos y gustos, y nos ayudan a ganar tiempo en las rutinas diarias</p>
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