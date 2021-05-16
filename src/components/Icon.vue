<template>
  <div class="contenedor">
        <ion-icon :name="icon"></ion-icon>
  </div>

</template>

<script>
export default {
  name: "Icon",
  props:{
    icon: String
  }
}
</script>

<style scoped>


.contenedor{
  border: 1px solid green;
  border-radius: 50px;
  font-size: 28px;
  height: 60px;
  width: 60px;
  text-align: center;
  padding-top: 12px;

}


ion-icon{
  color: #AAAAAA;
  text-align: center;


}

ion-icon:hover{
  color: green;

}



</style>
