
<template>
  <div id="main" class="flex-container">
    <div class="save__container flex-container">
      <img src="@/assets/cactus_logo.svg" alt>
      <p>¡Enhorabuena {{$route.params.userName}}!<br>Tu perfil ha sido actualizado.</p>
    </div>
  </div>
</template>

<script>
/* eslint-disable */

export default {
  data() {
    return {};
  },
  computed: {},
  mounted() {
    console.log("Save "+this.$route.params.userName+" in store");
    this.$store.userName = this.$route.params.userName
  }
};
</script>