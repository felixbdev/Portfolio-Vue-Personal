<template>
  <div class="col-12 col-md-3 card">
    <div class="icon">
      <ion-icon name="brush"></ion-icon>
    </div>
    <h5 class="title">{{title}}</h5>
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
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
}

.icon{
  margin-top: 20px;
  height: 30px;
}

.card:hover{
  background: rgba(0, 0, 0, 0.712);
}

.title,.text {
    color: #fff;
}

ion-icon{
  color: green;
  font-size: 50px;
}

</style>
