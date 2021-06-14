<template>
  <div class="contain mt-4">
    <h2>{{ tittle }}</h2>
    <p class="mt-3">{{ content }}</p>
  </div>
</template>

<script>
export default {
  name: "Content",
  components: {},
  props: {
    tittle: String,
    content: String
  }
};
</script>

<style scoped>
.contain {
  height: auto;
  width: 100%;
  margin: auto;
}

h2 {
  font-size: 2.8125rem;
  font-weight: 600;
}

p {
  font-size: 1.125rem;
  font-weight: 400;
  line-height: 1.875rem;
}
</style>
