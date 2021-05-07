<template>
  <div class="mt-2">
    <div class="progress" style="height: 2px;">
      <div class="progress-bar" role="progressbar" style="width: 25%;" :aria-valuenow="valor" aria-valuemin="0" aria-valuemax="100"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Barra',
  props: {
    valor: Number,
  }

}
</script>

