<template>
  <div class="row justify-content-center">
    <div class="button" v-for="button in button" :key="button.id">
      <button>{{button.language}}</button>
    </div>

    <div class="card mt-3 col-12 col-lg-3 justify-content-center " id="card-api" v-for="item in proyecto" :key="item.id">
      <h5>{{item.name}}</h5>
      <span>{{item.id}}</span>
      <span>{{item.language}}</span>
    </div>
  </div>

</template>

<script>
export default {
  name: "Proyectos",
  data(){
    return {
      proyecto: {},
      button:[],
    }
  },
  methods: {
    async consumirApi() {
      try {
        const data = await fetch ('https://api.github.com/users/felixbdev/repos')
        const object = await data.json()
        //console.log(object)
        this.proyecto = object
        this.button = object
        console.log(this.button)

      } catch (error) {
        console.log(error)
      }
    },
    filtrarArray(){
      console.log(this.button)
    }
  },
  created(){
    this.consumirApi()
    this.filtrarArray()
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
