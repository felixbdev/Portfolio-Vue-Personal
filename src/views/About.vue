<template>
  <div class="about">
    <div class="contact"></div>
    <div class="container-fluid background">
      <div class="row p-5 align-items-center">
        <div class="col-12 col-lg-6">
          <div class="container-image">
            <img src="../assets/about-me.jpg" alt="" class="img-thumbnail" />
          </div>
        </div>
        <div class="col-12 col-lg-6">
          <Content class="text-left text" tittle="Sobre mi" :content="about" />
        </div>
      </div>
    </div>

    <div class="container-fluid bienvenida text-white mt-2 p-5">
      <Content
        class="text-center"
        tittle="Que puedo aportar"
        :content="aporte"
      />
      <div class="row justify-content-around mt-5">
        <Cardimg
          :title="designer.titulo"
          :text="designer.descripcion"
          icon="/img/designer.png"
        />
        <Cardimg
        :title="brain.titulo"
        :text="brain.descripcion"
        icon="/img/brain.png" />
        <Cardimg
        :title="team.titulo"
        :text="team.descripcion"
        icon="/img/teamwork.png" />
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
import Content from "../components/Content";
import Cardimg from "../components/Cardimg";
import Footer from "../components/Footer";
import data from "../../informacion.json";

export default {
  name: "About",
  components: {
    Content,
    Cardimg,
    Footer
  },
  data() {
    return {
      about: ""
    };
  },
  created() {
    this.about = data.Aboutme.contenido;
    this.aporte = data.Aporte.contenido;
    this.designer = data.Aporte.designer;
    this.brain = data.Aporte.brain;
    this.team = data.Aporte.team;
  }
};
</script>

<style scoped>
.contact {
  background: #000; /* fallback for old browsers */
  height: 80px;
}

#Footer {
  background-color: #222222;
}

.bienvenida {
  background: #23232393; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to bottom,
    #00000083,
    #4642425b
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to bottom, #000000d7, #1211113f),
    url("../assets/bg-2.jpg"); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  background-attachment: fixed;
}

.background {
  background-color: #fca311;
}

.text {
  color: #000;
}

.container-image > img {
  border-radius: 0.08rem;
}
</style>
