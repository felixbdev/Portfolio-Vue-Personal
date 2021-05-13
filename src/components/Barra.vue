<template>
  <div class="mt-2">
    <div class="progress" style="height: 2px;">
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

