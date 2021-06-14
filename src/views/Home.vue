<template>
  <div>
    <div class="home container-fluid" id="portada">
      <div class="row">
        <div class="col-12 container hero">
          <Jumbotron
            titulo="Hola, soy Felix Bonillo"
            span="Desarrollador Front-End"
          />
        </div>
      </div>
    </div>

    <div class="container text-center scroll-content fadeTop" id="bienvenida">
      <div class="row">
        <div class="container col-12 mt-5">
          <Content
            class="text-black"
            :tittle="bienvenida.titulo"
            :content="bienvenida.contenido"
          />
        </div>
      </div>

      <div class="row mt-5 text-left">
        <div class="col-12 col-md-6 col-lg-4 mb-5 ">
          <span>HTML</span>
          <Barra :progres="85" />
        </div>
        <div class="col-12 col-md-6 col-lg-4 mb-5">
          <span>CSS</span>
          <Barra :progres="80" />
        </div>
        <div class="col-12 col-md-6 col-lg-4 mb-5">
          <span>Javascript</span>
          <Barra :progres="60" />
        </div>
      </div>

      <div class="row text-left mt-1">
        <div class="col-12 col-md-6 col-lg-4 mb-5">
          <span>Bootstrap</span>
          <Barra :progres="70" />
        </div>
        <div class="col-12 col-md-6 col-lg-4 mb-5">
          <span>Vue js</span>
          <Barra :progres="45" />
        </div>
        <div class="col-12 col-md-6 col-lg-4 mb-5">
          <span>Web Responsive</span>
          <Barra :progres="90" />
        </div>
      </div>
    </div>

    <div class="labores container-fluid mt-5 " id="Skills">
      <div class="container pt-2 scroll-content fadeTop">
        <Content
          :tittle="conocimientos.titulo"
          :content="conocimientos.contenido"
          class="text-white pt-4"
        />
        <div class="row justify-content-around mt-3 card-presentacion">
          <Card
            class="mb-2"
            title="Maquetado"
            text="Planificación, conceptualización y organización de contenido de un sitio web"
            icon="fas fa-paint-brush"
          />
          <Card
            class="mb-2"
            title="Control de versiones"
            text="Uso y manejo de control de versiones Git "
            icon="fab fa-git-alt"
          />
          <Card
            class="mb-5"
            title="Diseño Responsive"
            text="Sitio que responde de manera óptima cuando el usuario accede al sitio mediante dispositivos móviles. "
            icon="fas fa-mobile-alt"
          />
        </div>
      </div>
    </div>
    <div class="container-fluid proyectos fadeTop scroll-content mt-1">
      <div class="container pt-4 ">
        <h2>Proyectos</h2>
      </div>
      <Proyectos />
    </div>
    <div class="container-fluid mt-2" id="Experiencias">
      <div class="container fadeTop scroll-content prueba">
        <div class="row text-left">
          <div class="container col-12 col-md-6 mt-5 ">
            <div class="contain-titulo-experiencia mb-5">
              <h2>Educacion</h2>
            </div>
            <Experiencias
              class="mb-4"
              :fecha="educacion.universidad.fecha"
              :experiencia="educacion.universidad.titulo"
              resumen="Estudiante de 4° Trimestre en la carrera de informatica (Actual)"
            />
            <Experiencias
              class="mb-4"
              :fecha="educacion.cursojs.fecha"
              :experiencia="educacion.cursojs.titulo"
              :resumen="educacion.cursojs.descripcion"
            />
            <Experiencias
              class="mb-4"
              :fecha="educacion.cursocss.fecha"
              :experiencia="educacion.cursocss.titulo"
              :resumen="educacion.cursocss.descripcion"
            />
          </div>
          <div class="container col-12 col-md-6 mt-5">
            <div class="contain-titulo-experiencia mb-5">
              <h2>Experiencias</h2>
            </div>
            <Experiencias
              class="mb-4"
              :fecha="experiencia.portafolio.fecha"
              :experiencia="experiencia.portafolio.titulo"
              :resumen="experiencia.portafolio.descripcion"
            />
            <Experiencias
              class="mb-4"
              :fecha="experiencia.ListaTareas.fecha"
              :experiencia="experiencia.ListaTareas.titulo"
              :resumen="experiencia.ListaTareas.descripcion"
            />
            <Experiencias
              :fecha="experiencia.Carrito.fecha"
              :experiencia="experiencia.Carrito.titulo"
              :resumen="experiencia.Carrito.descripcion"
            />
          </div>
        </div>
      </div>
    </div>
    <div class="container-fluid mt-1" id="Footer">
      <div class="row">
        <div class="col-12">
          <Footer />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Jumbotron from "@/components/Jumbotron";
import Content from "@/components/Content";
import Barra from "../components/Barra";
import Card from "../components/Card";
import Proyectos from "../components/Proyectos";
import Experiencias from "../components/Experiencias";
import Footer from "../components/Footer";
import data from "../../informacion.json";

export default {
  name: "Home",
  components: {
    Jumbotron,
    Content,
    Barra,
    Card,
    Proyectos,
    Experiencias,
    Footer
  },created(){
    this.bienvenida = data.Bienvenida;
    this.conocimientos = data.Conocimientos;
    this.educacion = data.Educacion;
    this.experiencia = data.Experiencia;
  },


  mounted() {
    window.addEventListener("scroll", function() {
      let elements = document.getElementsByClassName("scroll-content");
      let screenSize = window.innerHeight;

      for (var i = 0; i < elements.length; i++) {
        let element = elements[i];

        if (element.getBoundingClientRect().top < screenSize) {
          element.classList.add("visible");
        } else {
          element.classList.remove("visible");
        }
      }
    });
  }
};
</script>

<style scoped>
.home {
  position: relative;
  background: #00000093; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to bottom,
    #43434361,
    #00000077
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to bottom, #00000071, #000000ad),
    url("../assets/fondojumbotron.jpg"); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  background-attachment: fixed;
  min-height: 100vh;
  width: 100%;
}

#Skills {
  background: #23232393; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to bottom,
    #0000009c,
    #4642425b
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to bottom, #00000079, #12111100),
    url("../assets/bg-3.jpg"); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  background-attachment: fixed;
  min-height: 100vh;
}

.proyectos {
  background: #fff;
  position: relative;
}

#Experiencias {
  background: #23232393; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to bottom,
    #00000098,
    #12111193
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to bottom, #000000bb, #121111af),
    url("../assets/bg-experiencias.jpg"); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  background-attachment: fixed;
  min-height: 100vh;
}

.contain-titulo-experiencia {
  color: #fff;
}

#Footer {
  background-color: #222222;
}

span {
  font-weight: 700;
}


h2 {
  font-size: 2.08125rem;
  font-weight: 600;
}


@media screen and (max-width: 991px){
  #Experiencias, #Skills {
    background-attachment: initial;
  }
}
</style>
