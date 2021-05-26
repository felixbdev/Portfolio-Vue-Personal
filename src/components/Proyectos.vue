<template>
  <div class="row justify-content-center p-3">
    <div class="button p-1 " v-for="(lenguaje, index) in button" :key="index">
      <button class="btn btn-outline-warning" @click="filtrar(lenguaje)">{{lenguaje}}</button>
    </div>
  </div>
  <div class="row justify-content-around">
    <div class="card mt-3 col-12 col-lg-3 justify-content-center mb-4" id="card-api" v-for="item in proyecto" :key="item.id">
      <div class="container">
        <h6>{{item.name}}</h6>
        <span>{{item.language}}</span>
      </div>
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


  .btn{
    background-color: e5e5e5;
  }

</style>
