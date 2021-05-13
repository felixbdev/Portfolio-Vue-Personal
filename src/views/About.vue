<template>
  <div class="about">
  </div>

<div class="container d-flex">
  <div class="img">
    <img src="../assets/avatar.png" alt="">
  </div>
  <Content 
  tittle= "Sobre mi"
  content= "loremdekiefkfekiefikefkfekifekifelsdfhhhhhhhhhhh" 
  />
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

.container{
  margin-top: 15px;
  flex-direction: column;
}

.img{
  height: auto;
  border: 1px solid blue;
  width: 290px;
  margin: 0px auto ;
}

.img img{
  width: 300px;
}


</style>