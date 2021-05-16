<template>
  <div class="contain">
    <h3>{{title}}</h3>
    <span>{{desde}}-{{hasta}}</span>

    <h5>{{experiencia}}</h5>
    <p>{{resume}}</p>
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

<style>

</style>
