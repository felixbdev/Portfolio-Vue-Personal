<template>
  <div class="col-12 col-md-3 card mt-5">
    <div class="icon">
      <ion-icon :name="icon"></ion-icon>
    </div>
    <h5 class="title">{{ title }}</h5>
    <p class="text">{{ text }}</p>
  </div>
</template>

<script>
export default {
  name: "CardWhote",
  props: {
    icon: String,
    title: String,
    text: String
  }
};
</script>

<style scoped>
.card {
  color: #000;
  background: #fff;
  height: 280px;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  border-radius: 10px;
    transition: ease-in-out;
  transition-duration: 0.5s;

}
.card:hover{
  background: #14213d;
  transform: translateY(-10px);
  box-shadow: 0px 10px 10px -6px black;
  color: #fff;
}
.icon {
  margin: 20px auto 5px;
  height: auto;
  width: 60px;

  border: 1px solid red;
}
h5:hover {
  color: green;
}


</style>
