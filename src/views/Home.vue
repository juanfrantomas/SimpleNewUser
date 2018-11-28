<template>
  <div id="main" class="flex-container">
    <div class="home__container flex-container">
      <img src="@/assets/cactus_logo.svg" width="50%" alt>
      <div id="input">
        <p>Inserta tu nombre</p>
        <input type="text">
      </div>
      <demo-button text="Entrar"></demo-button>
    </div>
  </div>
</template>
<script>
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
<style src="@/styles/main.css"></style>