<template>
  <div class="container">
    <div class="row contenedor-iconos container justify-content-center">
      <div class="contenedor-icon mr-2">
        <a href="https://github.com/felixbdev"><Icon class="centrado" icon="logo-github" /></a>
      </div>
      <div class="contenedor-icon mr-2">
        <a href="https://www.linkedin.com/in/felix-bonillo-7ba89a1bb/"><Icon class="centrado" icon="logo-linkedin"/></a>
      </div>
      <div class="contenedor-icon mr-2">
        <a href="https://www.instagram.com/felixbdev/"><Icon class="centrado" icon="logo-instagram" /></a>
      </div>
      <div class="contenedor-icon">
        <a href="https://twitter.com/felixbdev"><Icon class="centrado" icon="logo-twitter" /></a>
      </div>
    </div>
  </div>
  <hr />
  <div class="container">
    <div class="texto-footer">
      <p>
        © 2021 My Website. Sitio desarrollado con Vue js | Designed by
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
  height: 11.25rem;

}

.row {
  height: 4.375rem;
  margin: 0.75rem 0rem;

}

hr {
  background-color: #454545;
  height: 0.0063rem;
}

.texto-footer p {
  color: #aaaaaa;
}

.footer-link {
  text-decoration: none;
  color: whitesmoke;
  transition-duration: 0.4s;
}

.footer-link:hover {
  color: #fca311;


}

.centrado {
  margin: auto 0.1875rem;
}


</style>
