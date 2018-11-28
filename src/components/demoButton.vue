<template>
  <div 
  id="demo-button" 
  :style="`background-color:${color};`">
    <p>{{text}}</p>
  </div>
</template>
<script>
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
  width: 50%;
  cursor: pointer;
  padding: 2rem;
  border-radius: 6px;
  border: 1px solid #d8d8d8;
}
#demo-button p{
  font-size: 1.2rem;
}
</style>

