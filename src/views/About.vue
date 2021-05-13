<template>
  <div class="about">
  </div>

  <div class="container mt-5">
    <div class="row">
      <div class="img col-12 col-md-3">
        <img src="../assets/avatar.png" alt="">
      </div>
      <div class="col-12 col-md-9 d-flex align-items-center">
        <Content
          tittle= "Sobre mi"
          content= "loremdekiefkfekiefikefkfekifekifelsddsf sf
          wefwefwfw
          fwefwfwefhhhhhhhhhhh"
        />
      </div>
    </div>
  </div>
</template>


<script>
import Content from "../components/Content.vue"

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



.img{
  border: 1px solid blue;
  height: 300px;
  width: 100%;

}

.img img{
  width: 190px;
  height: 300px;
  object-fit: cover;
}


</style>
