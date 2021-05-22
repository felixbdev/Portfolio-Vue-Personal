<template>
  <div class="row justify-content-center m-4">
    <div class="button m-1 p-1 " v-for="(lenguaje, index) in button" :key="index">
      <button class="btn btn-outline-success" @click="filtrar(lenguaje)">{{lenguaje}}</button>
    </div>
  </div>
  <div class="row justify-content-center">

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
        this.proyecto = object
        object.forEach(element => {
          if (element.language) {
            this.button.push(element.language)
          }
        });
        this.filtrarArray()

      } catch (error) {
        console.log(error)
      }
    },
    filtrarArray(){
      let result = this.button.filter((item,index)=>{
        return this.button.indexOf(item) === index;
      })
      this.button = result
    },
    filtrar(lenguaje) {
      console.log(lenguaje.toLowerCase());
      console.log(this.item.language)

      }
  },
  created(){
    this.consumirApi()
  }
}
</script>

<style scoped>
  #card-api{
    padding: 15px;
    margin: 0px 30px;
    height: 230px;
  }

  .row{
    border: 1px solid red;
  }

</style>
