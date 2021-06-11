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
          <Content
            class="text-left text"
            tittle="About me"
            :content="about"
          />
          <div class="container-boton text-left mt-1">
            <Boton class="btn-lg " text="About me" />
          </div>
        </div>
      </div>
    </div>

    <div class="container-fluid bienvenida text-white mt-2 p-5">
      <Content
        class="text-center"
        tittle="Que puedo aportar"
        content="Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Nulla mollis dapibus nunc, ut rhoncus turpis sodales quis. Integer sit amet mattis qu
      am.Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Nulla mollis dapibus nunc"
      />
      <div class="row justify-content-around mt-5">
        <Cardimg icon="../assets/designer.png"/>
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
import Boton from "../components/Boton";
import Cardimg from "../components/Cardimg";
import Footer from "../components/Footer";
import data from '../../informacion.json';


export default {
  name: "About",
  components: {
    Content,
    Boton,
    Cardimg,
    Footer,
  },
  data(){
    return{
      about: ""
    }
  },
  created() {
    this.about = data.about_me
    console.log(data);
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
  background: #23232393;  /* fallback for old browsers */
  background: -webkit-linear-gradient(to bottom, #00000083, #4642425b);  /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to bottom, #000000d7, #1211113f), url("../assets/bg-2.jpg"); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  background-attachment: fixed;
}

.background{
  background-color: #fca311 ;
}

.text{
  color: #000;
}

.container-image > img{
  border-radius: 0.08rem;
}
</style>
