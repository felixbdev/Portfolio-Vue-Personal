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
#card-api {
  margin: 0.625rem 0.9375rem;
  padding: 0.9375rem;
  height: 14.375rem;
  background: #ffffffa8;
  color: #000;
  border-radius: 0.625rem;
  border: 0.125rem solid #000;
  transition: cubic-bezier(0.33, 0.6, 0.83, 0.67);
  transition-duration: 0.5s;
}

#card-api:hover {
  background: #14213d;
  color: #fff;
  transform: translateY(-10px);
  box-shadow: rgba(0, 0, 0, 0.09) 0rem 0.125rem 0.0625rem,
    rgba(0, 0, 0, 0.09) 0rem 0.25rem 0.125rem,
    rgba(0, 0, 0, 0.09) 0rem 0.5rem 0.25rem, rgba(0, 0, 0, 0.09) 0px 16px 8px,
    rgba(0, 0, 0, 0.09) 0px 32px 16px;
}

.btn {
  background: #fca311;
}

.btn:hover {
  color: white;
}

.img-card {
  height: 14.25rem;
  border-top-left-radius: 0.4375rem;
  border-bottom-left-radius: 0.5625rem;
  background: #14213d;
}

.img-card > img {
  position: relative;
  width: 6.875rem;
  margin-left: -1.0625rem;
  margin-top: 1.25rem;
}

span {
  font-size: 0.875rem;
  font-weight: 700;
}

h3 {
  font-size: 1rem;
  font-weight: 700;
}

p {
  font-size: 0.8125rem;
  font-weight: 300;
}

@media screen and (max-width: 720px) {
  span {
    font-size: 0.8125rem;
  }
  @media screen and (max-width: 568px) {
    span {
      font-size: 0.6875rem;
    }
  }
}
</style>
