<template>
  <div class="col-12 col-md-3 card mt-5">
    <div class="icon">
      <ion-icon :name="icon"></ion-icon>
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
  background: rgba(14, 4, 4, 0.541);
  height: 280px;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
}

.icon{
  margin: 20px auto 5px;
  height: auto;
  width: 60px;
}

h5{
  font-weight: bold;
}

.card:hover{
  background: #14213d
}

.title,.text {
    color: #fff;
}

ion-icon{
  color: #fca311;
  font-size: 50px;
}

</style>
