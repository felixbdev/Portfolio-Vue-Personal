<template class="container-sm" id= "countdown">
  <div class="container">
    <div class="clock text-white d-flex justify-content-around p-2">
      <div id="days col-12">
        <span class="days"></span>
        <h4>Dias</h4>
      </div>
      <div id="hours">
        <span class="hours"></span>
        <h4>Horas</h4>
      </div>
      <div id="minutes">
        <span class="minutes"></span>
        <h4>Minutos</h4>
      </div>
      <div id="seconds">
        <span class="seconds"></span>
        <h4>Segundos</h4>
      </div>
      <p class="text-white" id="clock"></p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Cuentaregresiva',
  methods: {
    clock:setInterval(()=>{
      let now = new Date().getTime()
      let countDownDate = new Date ("Jun 1, 2021 09:00:00").getTime()
      let distance = countDownDate - now
      let days = Math.floor(distance / (1000 * 60 * 60 * 24))
      let hours = Math.floor((distance % (1000 * 60 * 60 *24)) / (1000 * 60 *60))
      let minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60))
      let seconds = Math.floor((distance % (1000*60)) / 1000)
      //Pintar Resultados
      document.querySelector('.days').textContent = `${days}`
      document.querySelector('.hours').textContent = `${hours}`
      document.querySelector('.minutes').textContent = `${minutes}`
      document.querySelector('.seconds').textContent = `${seconds}`
    })
  }
}










</script>

<style>



.contenedor{
  margin:auto;
  border: 1px solid blue;
}

.clock span{
  text-align: center;
  font-size: 1.4rem;
  padding: 5px;
}

.clock h4{
  font-size: 1em;
}

.clock div{
  margin: auto;

}

</style>
