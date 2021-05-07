<template>
  <div class="col-12 col-md-3 mr-5 card">
    <div class="icon">
      <img :src="icon" alt="">
    </div>
    <span class="title">{{title}}</span>
    <p class="text">{{text}}</p>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props:{
    icon: String,
    title: String,
    text: String,
  }


}
</script>

<style scoped>
.card{
  background: rgba(164, 164, 164, 0.181);
  height: 300px;
}

.card:hover{
  background: rgba(0, 0, 0, 0.712);
}

.title,.text {
    color: #fff;
}




</style>
