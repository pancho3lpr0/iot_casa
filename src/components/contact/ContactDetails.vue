<template>
  <v-container fluid class="py-0 my-0 mt-0">
    <v-row class="py-0 my-0">
      <v-col md="9" sm="6" cols="12" class="py-0 my-0">
        <p
          class="google-font mb-1"
          style="font-size:110%"
        >Somos un grupo de estudiantes de TI en 4to grado en la Universidad Tecnologica del Oriente de Michoacan.</p>
        <p class="google-font">Domicilio: Comunidad de Santa Rita, Maravatio Mich s/n<br>
          Numero: 447-150-89-13<br>
          Email: <br>

        </p>
        <p class="google-font mt-5">Questions? Please contact {{data.email}}</p>
        <CommunitySocialInfo :config="config"  class="mb-2"/>
        <!--<span v-for="(item,i) in data.hashtags" :key="i" >
          <v-chip
            class="mr-1 mb-1"
            :href="'https://twitter.com/hashtag/'+item"
            target="_blank"
            label
          >#{{item}}</v-chip>
        </span>-->
      </v-col>
      <v-col md="3" sm="6" cols="12" class="py-0 my-0">
        <img :src="require('@/assets/img/svg/logo_contact.png')" style="float:right" width="80%" alt />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
// import SocialInfo from '@/components/common/SocialInfo'
import { mapState } from 'vuex'

export default {
  components:{
      CommunitySocialInfo : ()=>import('@/components/common/CommunitySocialInfo'),
    },
    data:()=>({
    }),
    computed:{
      ...mapState(['config'])
    },
  props: ["data"],
};
</script>