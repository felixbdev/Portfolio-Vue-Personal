<template>
  <div class="contain">
    <div class="contain-fecha mb-3 mt-1">
      <span>{{desde}} - {{hasta}}</span>
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
    desde: String,
    hasta: String,
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
    border: 0.125rem solid #fca311;
    width: 7.0625rem;
    text-align: center;
    padding: 0.125rem;
  }


  hr{
    background: whitesmoke;
    height: 0.0063rem;
    width: 94%;
    margin-left: 0rem;
  }

</style>
