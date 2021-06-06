<template>
  <div class="row justify-content-center p-3">
    <div class="button p-1 " v-for="(lenguaje, index) in button" :key="index">
      <button class="btn btn-outline-warning" @click="filtrar(lenguaje)">
        {{ lenguaje }}
      </button>
    </div>
  </div>
  <div class="row prueba container-fluid justify-content-around m-auto">
    <div
      class="card mt-3 col-12 col-lg-3 justify-content-center mb-4"
      id="card-api"
      v-for="item in proyecto"
      :key="item.id"
    >
      <div class="row">
        <div class="col-4 img-card m-auto">
          <img src="../assets/card-api.png" alt="" />
          <div class="contain mt-3">
            <span class="text-white font-weight-bold">{{ item.language }}</span>
          </div>
        </div>
        <div class="col-8 p-2 mt-2">
          <div class="container text-left">
            <h3 class="font-weight-bold">{{ item.name }}</h3>
            <p>{{ item.description }}</p>
          </div>
          <div class="container text-left">
            <button class="btn" @click="ir(item.html_url)">Ver codigo</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Proyectos",
  data() {
    return {
      proyecto: {},
      button: []
    };
  },
  methods: {
    async consumirApi() {
      try {
        const data = await fetch(
          "https://api.github.com/users/felixbdev/repos"
        );
        const object = await data.json();
        this.proyecto = object;
        //console.log(object);
        /*object.forEach(element => {
          if (element.language) {
            this.button.push(element.language)
          }
        });
        this.filtrarArray()*/
      } catch (error) {
        console.log(error);
      }
    },
    /*filtrarArray(){
      let result = this.button.filter((item,index)=>{
        return this.button.indexOf(item) === index;
      })
      this.button = result
    },
    filtrar(lenguaje) {
      console.log(lenguaje);
      console.log(this.proyecto)
      }*/
    ir(url) {
      console.log(url);
      let abrir = window.open(url, "-black");
      abrir.focus();
    }
  },
  created() {
    this.consumirApi();
  }
};
</script>

<style scoped>
*{
  font-size: 13px;
}


#card-api {
  margin: 10px 15px;
  padding: 15px;
  height: 230px;
  background: #ffffffa8;
  color: #000;
  border-radius: 10px;
  border: 2px solid #000;
  transition: ease-in-out;
  transition-duration: 0.5s;
}

#card-api:hover {
  background: #14213d;
  color: #fff;
  transform: translateY(-10px);
  box-shadow: rgba(0, 0, 0, 0.09) 0px 2px 1px, rgba(0, 0, 0, 0.09) 0px 4px 2px, rgba(0, 0, 0, 0.09) 0px 8px 4px, rgba(0, 0, 0, 0.09) 0px 16px 8px, rgba(0, 0, 0, 0.09) 0px 32px 16px;
}



.btn {
  background: #fca311;
}

.btn:hover {
  color: white;
}

.img-card{

  height: 228px;
  border-top-left-radius: 7px;
  border-bottom-left-radius: 9px;
  background: #14213d;
}


.img-card > img{
  position: relative;
  width: 110px;
  margin-left: -17px;
  margin-top: 20px;

}
</style>
