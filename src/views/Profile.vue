
<template>
  <div id="main" class="flex-container">
    <div class="profile__container flex-container">
      <!-- Ficha de Usuario -->
      <div class="profile__section primary">
        <h2>FICHA DE USUARIO</h2>
        <div class="profile__section__content">
          <div id="output">
            <p>Nombre:</p>
            <div>
              {{this.name}}
            </div>
          </div>
          <div id="output">
            <p>Apellidos:</p>
            <div>
              {{this.surname}}
            </div>
          </div>
          <div id="output">
            <p>Descripción:</p>
            <div class="description">
              {{this.desc}}
            </div>
          </div>
          <button v-show="name || surname || desc" @click="cleanAll">Borrar todo</button>
        </div>
        <div class="profile__section__aside">
          <h2>SOCIAL</h2>
          <div class="logo-container">
            <!-- El simbolo se mostrará aquí -->
            <div v-for="(icon,key) in icons" :key="key">
              <a :href="icon.url" :style="{'text-decoration':'none'}">
                <img :src="icon.svg" alt="">
                <h4>{{icon.title}}</h4>
              </a>
            </div>
            <!-- El título (h4) se mostrará aquí -->
          </div>
        </div>
      </div>
      <hr>
      <!-- Introducción de Datos -->
      <div class="profile__section secondary">
        <div class="profile__section__content">
          <div id="input" class="name" >
            <p>Nombre</p>
            <input type="text" v-model="name" ref="name">
          </div>
          <div id="input" class="surname" >
            <p>Apellidos</p>
            <input type="text" v-model="surname" ref="surname">
          </div>
          <div id="textarea" class="description">
            <p>Descripción</p>
            <textarea v-model="desc" ref="desc" ></textarea>
          </div>
        </div>
        <div class="profile__section__aside">
          <demo-button @click.native="congratulations"
          text="Guardar"
          color="#9fd356"
          ></demo-button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
/* eslint-disable */
import demoButton from "@/components/demoButton";

export default {
  data() {
    return {  
      icons: [
        {
          title: "WEBSITE",
          url: "https://www.wearecactus.com",
          svg: require('@/assets/icons/cactus-symbol.svg')
        },
        {
          title: "INSTAGRAM",
          url: "https://www.instagram.com/wearecactus/",
          svg: require('@/assets/icons/ig-symbol.svg')
        },
        {
          title: "LINKEDIN",
          url: "https://es.linkedin.com/company/cactus-agency",
          svg: require('@/assets/icons/linkedin-symbol.svg')
        },
        {
          title: "TWITTER",
          url: "https://twitter.com/wearecactus",
          svg: require('@/assets/icons/twitter-symbol.svg')
        }
      ],
      name: '',
      surname: '',
      desc: '',
      svg:''
    };
  },
  components: {
    demoButton
  },
  computed: {},
  methods: {
    cleanAll () {
      this.name = this.surname = this.desc = "";
    },
    congratulations () {
      this.$router.push({name: 'Save', params: {userName: this.name}});
    }
  }
};
</script>