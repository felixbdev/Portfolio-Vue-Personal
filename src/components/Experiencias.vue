<template>
  <div class="contain">
    <div class="contain-fecha mb-3 mt-1">
      <span>{{desde}}-{{hasta}}</span>
    </div>
    <div class="contain-title-experiencia mb-3">
      <h5>{{experiencia}}</h5>
    </div>
    <div class="contain-resume-experiencia">
      <p>{{resumen}}</p>
    </div>
    <hr>
  </div>

</template>

<script>
export default {
  name: "Experiencias",
  props:{
    title: String,
    desde: Number,
    hasta: Number,
    experiencia: String,
    resumen: String
  }

}
</script>

<style scoped>
  .contain{
    color: #fff;
  }

  .contain-fecha{
    border: 2px solid green;
    width: 100px;
    text-align: center;
  }

  hr{
    background: whitesmoke;
    height: .1px;
    width: 94%;
    margin-left: 0px;
  }

</style>
