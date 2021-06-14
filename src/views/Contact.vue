<template>
  <div class="contenedor">
    <div class="contact"></div>
    <div class="container-fluid contact-us">
      <div class="row p-2">
        <div class="col-12 col-md-6">
          <Formulario />
        </div>
        <div class="col-12 col-md-6 align-middle mt-4">
          <div class="container-img align-middle">
            <img class="rounded" src="../assets/notificacion.png" alt="" />
          </div>
        </div>
      </div>
    </div>

    <div class="container-fluid" id="Footer">
      <div class="row">
        <div class="col-12">
          <Footer />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Formulario from "../components/Formulario";
import Footer from "../components/Footer";

export default {
  name: "Contact",
  components: {
    Formulario,
    Footer
  }
};
</script>

<style scoped>
.contact {
  background: #000; /* fallback for old browsers */
  height: 80px;
}

img {
  width: 100%;
}

.contact-us {
  padding-bottom: 150px;
}

.contenedor {
  min-height: 100vh;
  position: relative;
  width: 100%;
}

#Footer {
  background-color: #222222;
  position: absolute;
  bottom: 0;
  height: 180px;
  width: 100%;
}
</style>
