<template>
  <div class="row">
    <div class="col-12">
      <div class="jumbotron bg-transparent mt-5">
        <div class="contenedor-img mt-5">
          <!-- <img src="../assets/avatar.jpg" :alt="text" class="img-thumbnail"> -->
          <img
            id="img"
            :src="require('@/assets/avatar.png')"
            :alt="text"
            class="img-thumbnail rounded-circle"
          />
        </div>
        <div class="info">
          <h1 class="display-5 texto-blanco mt-4">{{ titulo }}</h1>
          <p class="lead text-white">{{ span }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Jumbotron",
  components: {},
  props: {
    titulo: String,
    span: String
  },
  data() {
    return {
      image: "../assets/avatar.jpg",
      text: "Avatar"
    };
  }
};
</script>

<style scoped>
.texto-blanco {
  color: white;
  font-size: 2.8125rem;
  font-weight: 700;
}

.lead {
  font-weight: 400 italic;
  font-size: 1.5625rem;
}

#img {
  width: 10.625rem;
}
</style>
