<template>
        <div>
          <h2>{{tittle}}</h2>
          <p class="mt-4">{{content}}</p>
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
.container{
  height: auto;
  width: 850px;

}

</style>
