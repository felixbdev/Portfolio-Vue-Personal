<template>
  <div class="col-12 col-md-3 card mt-5">
    <div class="icon">
      <i :class="icon"></i>
    </div>
    <h5 class="title">{{ title }}</h5>
    <p class="text">{{ text }}</p>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    icon: String,
    title: String,
    text: String
  }
};
</script>

<style scoped>
.card {
  background: rgba(14, 4, 4, 0.541);
  border-radius: 0.625rem;
  height: 17.5rem;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  transition: cubic-bezier(0.33, 0.6, 0.83, 0.67);
  transition-duration: 0.3s;
}

.icon {
  margin: 1.25rem auto 0.3125rem;
  height: auto;
  width: 3.75rem;
}

h5 {
  font-weight: 700;
}

p {
  font-weight: 400;
}

.card:hover {
  background: #14213d;
  box-shadow: rgba(0, 0, 0, 0.19) 0px 10px 20px, rgba(0, 0, 0, 0.23) 0px 6px 6px;
}

.title,
.text {
  color: #fff;
}

i {
  font-size: 3.75rem;
  color: #fca311;
}
</style>
