<template>
  <div class="about"></div>
  <div class="container mt-4">
    <div class="row">
      <div class="col-12">
        <div class="container-image">
          <img src="../assets/about-me.jpg" alt="" class="img-thumbnail">
        </div>
      </div>
      <div class="col-12">
        <Content
        class="text-left"
        tittle= "About me"
        />
      </div>
    </div>
  </div>

</template>


<script>
  import Content from '../components/Content'


export default {

  name: "About",
  components: {
    Content
  }
}
</script>






<style scoped>

.about {
  background: #00000093;  /* fallback for old browsers */
  background: -webkit-linear-gradient(to right, #434343, #00000069);  /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to right, #00000070, #00000067), url("../assets/bg-about.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  height: 100px;

}





</style>


