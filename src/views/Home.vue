<template>
  <div class="home container-fluid">
    <div class="row">
      <div class="col-12 container hero">
            <Jumbotron titulo= "Hello, I'm Felix Bonillo" span = "Desarrollador Front-End"/>
      </div>
    </div>
  </div>
  <div class="container text-center">
    <div class="row">
      <div class="container col-12">
        <Content
          class="text-black"
          tittle='Welcome To my Site'
          content="Vestibulum ante ipsum primis in faucibus orci luctus et
          ultrices posuere cubilia Curae; Nulla mollis dapibus nunc, ut rhoncus turpis
          sodales quis. Integer sit amet mattis quam.Vestibulum ante ipsum primis in faucibus
          orci luctus et ultrices posuere cubilia Curae; Nulla mollis dapibus nunc"
        />
      </div>
    </div>
    <div class="row mt-5 text-left">
      <div class="col-12 col-md-6 col-lg-4 mb-5 ">
        <span>HTML</span>
        <Barra/>
      </div>
      <div class="col-12 col-md-6 col-lg-4 mb-5">
        <span>CSS</span>
        <Barra/>
      </div>
      <div class="col-12 col-md-6 col-lg-4 mb-5">
        <span>Javascript</span>
        <Barra/>
      </div>
    </div>

    <div class="row text-left">
      <div class="col-12 col-md-6 col-lg-4 mb-5">
        <span>Bootstrap</span>
        <Barra/>
      </div>
      <div class="col-12 col-md-6 col-lg-4 mb-5">
        <span>Vue js</span>
        <Barra/>
      </div>
      <div class="col-12 col-md-6 col-lg-4 mb-5">
        <span>Web Responsive</span>
        <Barra/>
      </div>
    </div>

    </div>

    <div class="container-fluid labores bg-danger" >
      <Content
      tittle="I'm Available For Hire"
      content="Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere
      cubilia Curae; Nulla mollis dapibus nunc, ut rhoncus turpis sodales quis. Integer sit amet mattis quam."
      class="text-white pt-5"
      />
      <div class="row justify-content-center mt-3 card-presentacion">
        <Card
        title="Frontend"
        text="Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Nulla mollis dapibus nunc"
        />
        <Card
        title="Maquetador"
        text="Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Nulla mollis dapibus nunc"
        />
        <Card
        title="Nuevas Tecnologias"
        text="Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Nulla mollis dapibus nunc"
        />
      </div>

  </div>



</template>

<script>
import Jumbotron from '@/components/Jumbotron'
import Content from '@/components/Content'
import Barra from '../components/Barra'
import Card from '../components/Card'

export default {
  name: 'Home',
  components: {
    Jumbotron,Content,Barra,Card
  }
}
</script>

<style scoped>

.home{
  position: relative;
  background: #00000093;  /* fallback for old browsers */
  background: -webkit-linear-gradient(to right, #434343, #000000);  /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to right, #000000a4, #000000d7), url("../assets/fondojumbotron.jpg"); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  background-attachment: fixed;
  min-height: 100vh;
}

.labores{
    background: #23232393;  /* fallback for old browsers */
  background: -webkit-linear-gradient(to bottom, #434343, #535353);  /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to bottom, #00000083, #4642425b), url("../assets/bg-3.jpg"); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  background-attachment: fixed;
  min-height: 100vh;
}

</style>
