
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
              <!-- El contenido se mostrará aquí -->
            </div>
          </div>
          <div id="output">
            <p>Apellidos:</p>
            <div>
              <!-- El contenido se mostrará aquí -->
            </div>
          </div>
          <div id="output">
            <p>Descripción:</p>
            <div class="description">
              <!-- El contenido se mostrará aquí -->
            </div>
          </div>
          <button>Borrar todo</button>
        </div>
        <div class="profile__section__aside">
          <h2>SOCIAL</h2>
          <div class="logo-container">
            <!-- El simbolo se mostrará aquí -->
            <!-- El título (h4) se mostrará aquí -->
          </div>
        </div>
      </div>
      <hr>
      <!-- Introducción de Datos -->
      <div class="profile__section secondary">
        <div class="profile__section__content">
          <div id="input" class="name">
            <p>Nombre</p>
            <input type="text">
          </div>
          <div id="input" class="surname">
            <p>Apellidos</p>
            <input type="text">
          </div>
          <div id="textarea" class="description">
            <p>Descripción</p>
            <textarea></textarea>
          </div>
        </div>
        <div class="profile__section__aside">
          <demo-button
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
    return {};
  },
  components: {
    demoButton
  },
  computed: {}
};
</script>