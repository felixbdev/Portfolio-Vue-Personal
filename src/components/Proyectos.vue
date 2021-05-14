<template>
  <div class="row justify-content-center">
    <div class="card mt-3 col-12 col-lg-3 justify-content-center " id="card-api" v-for="item in proyecto" :key="item.id">
      <h5>{{item.name}}</h5>
      <span>{{item.id}}</span>
    </div>
  </div>

</template>

<script>
export default {
  name: "Proyectos",
  data(){
    return {
      proyecto: {}
    }
  },
  methods: {
    async consumirApi() {
      try {
        const data = await fetch ('https://api.github.com/users/felixbdev/repos')
        const object = await data.json()
        console.log(object)
        this.proyecto = object
      } catch (error) {
        console.log(error)
      }
    }
  },
  created(){
    this.consumirApi()
  }
}
</script>

<style>
  #card-api{
    padding: 15px;
    margin: 0px 30px;
    height: 230px;
  }

  .row{
    border: 1px solid red;
  }

</style>
