<template>
  <div class="mt-2">
    <div class="progress" style="height: 3px;">
      <div class="progress-bar" :style = "{'width': progres+'%'}" role="progressbar" :aria-valuenow="progres" aria-valuemin="0" aria-valuemax="100"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Barra',
  props: {
    progres: Number,

  }

}
</script>

<style scoped>
.progress-bar{
  background: #11998e;  /* fallback for old browsers */
  background: -webkit-linear-gradient(to right, #38ef7d, #11998e);  /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to right, #38ef7d, #11998e); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */

}
</style>

