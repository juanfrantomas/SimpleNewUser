<template>
  <div id="main" class="flex-container">
    <div class="home__container flex-container">
      <img src="@/assets/cactus_logo.svg" alt>
      <div id="input">
        <p>Inserta tu nombre</p>
        <input type="text">
      </div>
      <demo-button
      text="Entrar"
      size="50%"
      ></demo-button>
    </div>
  </div>
</template>
<script>
/* eslint-disable */
import demoButton from "@/components/demoButton";
export default {
  data() {
    return {};
  },
  components: {
    demoButton
  },
  computed: {}
};
</script>