<template>
  <div id="main" class="flex-container">
    <div class="home__container flex-container">
      <img src="@/assets/cactus_logo.svg" alt>
      <div id="input">
        <p>Inserta tu nombre</p>
        <input type="text" v-model="username">
      </div>
      <demo-button
      text="Entrar"
      size="50%"
      :color=color
      @click.native="inputValidate"></demo-button>
    </div>
  </div>
</template>
<script>
/* eslint-disable */
import demoButton from "@/components/demoButton";
import { setTimeout } from 'timers';
export default {
  data() {
    return {
      username: '',
      color: '#d8d8d8'
    };
  },
  components: {
    demoButton
  },
  computed: {},
  methods: {
    inputValidate: function (event) {
      if(!this.username){
        this.color = '#f37d7d';
      }else{
        this.color = '#9dd258';
        setTimeout(()=>{
          this.$router.push('Profile');
        },500);
      }
    }
  }

};
</script>