<template>
  <div class="contain">
    <div class="text-center">
        <h2>{{tittle}}</h2>
        <p class="mt-4">{{content}}</p>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Content',
  components:{
  },
  props:{
    tittle: String,
    content: String
  },
}
</script>

<style scoped>
.contain{
  height: auto;
  width: 100%;
  margin: auto;
  border: 1px solid red;

}

h2{
  font-weight: bold;
}

</style>
