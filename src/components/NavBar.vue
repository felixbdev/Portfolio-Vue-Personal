<template>
  <div id="nav" @click="closeNavbar">
    <nav class="navbar navbar-expand-lg navbar-dark ">
      <a class="navbar-brand" href="/">Felix Bonillo</a>
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <div
        class="collapse navbar-collapse rastreador"
        id="navbarSupportedContent"
      >
        <ul class="navbar-nav ml-auto text-left mt-2">
          <li class="nav-item active">
            <router-link class="link" to="/">Inicio</router-link>
          </li>
          <li class="nav-item">
            <router-link class="link" to="/about">Sobre mi</router-link>
          </li>
          <li class="nav-item">
            <router-link class="link" to="/contact">Contacto</router-link>
          </li>
        </ul>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "NavBar",
  components: {},
  methods: {
    widthScreen() {
      const width = screen.width;
      //console.log(width)
      const colorNav = document.getElementById("navbarSupportedContent");
      //console.log(colorNav)
      if (width <= 991) {
        //console.log('Es menor')
        colorNav.classList.add("bg-dark");
      }
    },
    closeNavbar(e) {
      const showNavbar = document.getElementById("navbarSupportedContent");
      //console.log(e.target)
      if (
        e.target.classList.contains("nav-item") ||
        e.target.classList.contains("router-link-active")
      ) {
        showNavbar.classList.toggle("show");
      }
    }
  },
  mounted() {
    this.widthScreen();
  }
};
</script>

<style scoped>
#nav {
  background-color: transparent;
  position: absolute;
  width: 100%;
  z-index: 1;
}

#nav .dropdown-menu {
  background: transparent;
  border: none;
}

#nav {
  padding: 0.625rem;
}

#nav li {
  padding: 0.25rem 0.625rem;
  margin-left: 0.375rem;
}

.link {
  color: #fff;
  text-decoration: none;
  margin-right: 0.875rem;
  font-weight: 600;
}

#nav a.router-link-exact-active {
  color: #fca311;
}

#nav .navbar-brand {
  color: #fff;
}

#nav .navbar-brand:hover {
  color: #fca311;
}

.navbar-brand {
  font-weight: 700;
  transition: ease;
  transition-duration: 0.4s;
}
</style>
