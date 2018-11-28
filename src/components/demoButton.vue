<template>
  <div id="demo-button" :style="`width:${size};background-color:${color};`">
    <p>{{text}}</p>
  </div>
</template>
<script>
/* eslint-disable */
export default {
  name: "demo-button",
  data() {
    return {};
  },
  props: {
    text: {
      type: String,
      default: "button"
    },
    color: {
      type: String,
      default: "#d8d8d8"
    },
    size: {
      type: String,
      default: "100%"
    }
  },
  computed: {}
};
</script>
<style scoped>
p {
  margin: 0;
}
#demo-button {
  cursor: pointer;
  padding: 2rem;
  border-radius: 6px;
  border: 1px solid #d8d8d8;
}
#demo-button p {
  font-size: 1.2rem;
}
</style>

