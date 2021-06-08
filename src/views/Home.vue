<template>
  <div class="home container-fluid" id="portada">
    <div class="row">
      <div class="col-12 container hero">
        <Jumbotron titulo= "Hola, soy Felix Bonillo" span = "Desarrollador Front-End"/>
      </div>
    </div>
  </div>

  <div class="container text-center" id="bienvenida">
    <div class="row">
      <div class="container col-12 mt-5">
        <Content
          class="text-black"
          tittle='Bienvenido a mi sitio'
          content="Es un placer darte la bienvenida a mi portafolio, en el cual encontrar informacion sobre mi formacion academica
          , sobre los trabajos que he realizado de manera individual desarrollando mis capacidades y habilidades, actualmente soy
          estudiante universitario de la carrera de informatica."
        />
      </div>
    </div>


    <div class="row mt-5 text-left">
      <div class="col-12 col-md-6 col-lg-4 mb-5 ">
        <span>HTML</span>
        <Barra
        :progres="85"
        />
      </div>
      <div class="col-12 col-md-6 col-lg-4 mb-5">
        <span>CSS</span>
        <Barra
          :progres="80"
        />
      </div>
      <div class="col-12 col-md-6 col-lg-4 mb-5">
        <span>Javascript</span>
        <Barra
        :progres="60"
        />
      </div>
    </div>




    <div class="row text-left mt-1">
      <div class="col-12 col-md-6 col-lg-4 mb-5">
        <span>Bootstrap</span>
        <Barra
          :progres="70"
        />
      </div>
      <div class="col-12 col-md-6 col-lg-4 mb-5">
        <span>Vue js</span>
        <Barra
        :progres="45"
        />
      </div>
      <div class="col-12 col-md-6 col-lg-4 mb-5">
        <span>Web Responsive</span>
        <Barra
        :progres="90"
        />
      </div>
    </div>
  </div>


  <div class="labores container-fluid bg-danger mt-5" id="skills">
    <div class="container pt-2 ">
      <Content
        tittle="Tengo conocimientos extras"
        content="Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere
        cubilia Curae; Nulla mollis dapibus nunc, ut rhoncus turpis sodales quis. Integer sit amet mattis quam."
        class="text-white pt-4"
      />
      <div class="row justify-content-around mt-5 card-presentacion">
        <Card
          class="mb-2"
          title="Maquetado"
          text="Planificación, conceptualización y organización de contenido de un sitio web"
          icon="brush"
        />
        <Card
          class="mb-2"
          title="Control de versiones"
          text="Uso y manejo de control de versiones Git "
          icon="git-branch-sharp"
        />
        <Card
          class="mb-5"
          title="Diseño Responsive"
          text="Sitio que responde de manera óptima cuando el usuario accede al sitio mediante dispositivos móviles. "
          icon="tv-outline"
        />
      </div>
    </div>
  </div>
  <div class="container-fluid proyectos mt-1 mb-2">
    <div class="container pt-4">
      <h2>Proyectos</h2>
    </div>
    <Proyectos
    />
  </div>
  <div class="container-fluid mt-2" id="Experiencias">
    <div class="container">
      <div class="row text-left">
        <div class="container col-12 col-md-6 mt-5">
          <div class="contain-titulo-experiencia mb-5">
            <h2>Educacion</h2>
          </div>
          <Experiencias
            class="mb-4"
            desde=2020
            hasta="Actual"
            experiencia="Instituto Universitario de Mercadotecnia ISUM"
            resumen="Estudiante de 4° Trimestre en la carrera de informatica (Actual)"
          />
          <Experiencias
            class="mb-4"
            desde=2020
            hasta=2021
            experiencia="Jóvenes Programadores de BiblioRedes"
            resumen="Certificado Javascript I"
          />
          <Experiencias
            class="mb-4"
            desde="2020"
            hasta="2021"
            experiencia="Jóvenes Programadores de BiblioRedes"
            resumen="Certificado CSS"
          />
        </div>
        <div class="container col-12 col-md-6 mt-5">
          <div class="contain-titulo-experiencia mb-5">
            <h2>Experiencias</h2>
          </div>
          <Experiencias
            class="mb-4"
            desde=2021
            hasta="Actual"
            experiencia="Portafolio Personal"
            resumen="Portafolio personal realizado con Vue js poniendo en practica mis destrezas y habilidades en el manejo de componentes."
          />
          <Experiencias
            class="mb-4"
            desde="Abril"
            hasta=2021
            experiencia="Lista de Tareas"
            resumen="App para registrar tareas pendientes y realizadas con Javascript"
          />
          <Experiencias
            desde="Abril"
            hasta=2021
            experiencia="Carrito de compras"
            resumen="Realización de carrito de compras con sistema CRUD en Javascript"
          />
        </div>
      </div>
    </div>
  </div>
  <div class="container-fluid mt-2" id="Footer">
    <div class="row">
      <div class="col-12">
        <Footer/>
      </div>
    </div>
  </div>
</template>

<script>
import Jumbotron from '@/components/Jumbotron'
import Content from '@/components/Content'
import Barra from '../components/Barra'
import Card from '../components/Card'
import Proyectos from '../components/Proyectos'
import Experiencias from '../components/Experiencias'
import Footer from '../components/Footer'


export default {
  name: 'Home',
  components: {
    Jumbotron,Content,Barra,Card, Proyectos,Experiencias,Footer
  },
}
</script>

<style scoped>

.home{
  position: relative;
  background: #00000093;  /* fallback for old browsers */
  background: -webkit-linear-gradient(to bottom, #43434361, #00000077);  /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to bottom, #00000071, #000000ad), url("../assets/fondojumbotron.jpg"); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  background-attachment: fixed;
  min-height: 100vh;
}

.labores{
  background: #23232393;  /* fallback for old browsers */
  background: -webkit-linear-gradient(to bottom, #0000009c, #4642425b);  /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to bottom, #00000079, #12111100), url("../assets/bg-3.jpg"); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  background-attachment: fixed;
  min-height: 100vh;
}

.proyectos{
  background: #fff;
}

#Experiencias{
  background: #23232393;  /* fallback for old browsers */
  background: -webkit-linear-gradient(to bottom, #00000098, #12111193);  /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to bottom, #000000bb, #121111af), url("../assets/bg-experiencias.jpg"); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  background-attachment: fixed;
  min-height: 100vh;
}

.contain-titulo-experiencia{
  color: #fff;
}

#Footer{
    background-color: #222222;
}

span{
  font-weight: 700;
}

h2{
    font-size: 2.8125rem;
  font-weight: 600;
}

</style>
