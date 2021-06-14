<template>
  <button class="btn">
    {{ text }}
  </button>
</template>

<script>
export default {
  name: "Boton",
  props: {
    text: String
  }
};
</script>

<style scoped>
.btn {
  background-color: #14213d;
  color: white;
}

.btn:hover {
  color: #fca311;
}
</style>
