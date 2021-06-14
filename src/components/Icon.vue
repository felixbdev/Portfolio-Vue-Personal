<template>
  <div class="contenedor">
    <i :class="icon"></i>
  </div>
</template>

<script>
export default {
  name: "Icon",
  props: {
    icon: String
  }
};
</script>

<style scoped>
.contenedor {
  border: 0.5px solid rgba(255, 255, 255, 0.26);
  border-radius: 3.125rem;
  font-size: 1.75rem;
  height: 3.75rem;
  width: 3.75rem;
  text-align: center;
  padding-top: 0.75rem;
}

i {
  color: #aaaaaa;
  text-align: center;
  cursor: pointer;
  transition: ease-in;
  transition-duration: 0.2s;
}

i:hover {
  color: #fca311;
}
</style>
