<template>
  <div class="about"></div>
  <div class="container mt-4">
    <div class="row p-3 align-items-center">
      <div class="col-12 col-lg-6">
        <div class="container-image">
          <img src="../assets/about-me.jpg" alt="" class="img-thumbnail" />
        </div>
      </div>
      <div class="col-12 col-lg-6">
        <Content
          class="text-left mt-4"
          tittle="About me"
          content="Lorem ipsum dolor sit, amet consectetur adipisicing elit. Amet non porro laboriosam rerum fugiat quod ullam earum dignissimos corporis, nemo provident nostrum, nihil culpa. Et corrupti sit hic amet, animi unde cumque consequuntur omnis ad nihil optio id eum qui, impedit deleniti? Veniam eum aspernatur incidunt? Doloremque, cum? Repellendus consectetur, cupiditate tenetur provident neque, quas, totam eveniet nisi eius veritatis ea maiores ducimus a reprehenderit minima magnam dicta! Aliquam
          libero voluptatum facilis dolorum architecto? Doloribus fuga voluptate voluptatem corporis rem! Culpa nam et accusamus beatae!"
        />
        <div class="container-boton text-left mt-1">
          <Boton class="btn-lg " text="About me" />
        </div>
      </div>
    </div>
  </div>

  <div class="container-fluid bienvenida mt-5">
    <div class="container">
      <Content
        class="text-center"
        tittle="Welcome To My Site"
        content="Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Nulla mollis dapibus nunc, ut rhoncus turpis sodales quis. Integer sit amet mattis qu
    am.Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Nulla mollis dapibus nunc"
      />
      <div class="row justify-content-around">
        <CardWhite />
        <CardWhite />
        <CardWhite class="mb-5" />
      </div>
    </div>
  </div>

  <div class="container-fluid mt-5" id="Footer">
    <div class="row">
      <div class="col-12">
        <Footer />
      </div>
    </div>
  </div>
</template>

<script>
import Content from "../components/Content";
import Boton from "../components/Boton";
import CardWhite from "../components/CardWhite";
import Footer from "../components/Footer";

export default {
  name: "About",
  components: {
    Content,
    Boton,
    CardWhite,
    Footer
  }
};
</script>

<style scoped>
.about {
  background: #00000093; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to right,
    #434343,
    #00000069
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to right, #00000070, #00000067),
    url("../assets/bg-about.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  height: 100px;
}

#Footer {
  background-color: #222222;
}

.bienvenida {
  background: #edf6f9;
}
</style>
