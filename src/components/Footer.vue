<template>
  <div class="container">
    <div class="row contenedor-iconos container justify-content-center">
      <div class="contenedor-icon mr-2">
        <Icon class="centrado" icon="logo-gitlab" />
      </div>
      <div class="contenedor-icon mr-2">
        <Icon class="centrado" icon="logo-gitlab" />
      </div>
      <div class="contenedor-icon mr-2">
        <Icon class="centrado" icon="logo-gitlab" />
      </div>
      <div class="contenedor-icon">
        <Icon class="centrado" icon="logo-gitlab" />
      </div>
    </div>
  </div>
  <hr />
  <div class="container">
    <div class="texto-footer">
      <p>
        © 2021 My Website. All rights reserved | Designed by
        <a class="footer-link" href="https://github.com/felixbdev"
          >Felixbdev</a
        >
      </p>
    </div>
  </div>
</template>

<script>
import Icon from "../components/Icon";
export default {
  name: "Footer",
  components: {
    Icon
  }
};
</script>

<style scoped>
#footer {
  height: 180px;

}

.row {
  height: 70px;
  margin: 12px 0px;
  padding: 0px;
}

hr {
  background-color: #454545;
  height: 0.1px;
}

.texto-footer p {
  color: #aaaaaa;
}

.footer-link {
  text-decoration: none;
  color: whitesmoke;
}

.footer-link:hover {
  color: green;
}

.centrado {
  margin: auto 10px;
}


</style>
