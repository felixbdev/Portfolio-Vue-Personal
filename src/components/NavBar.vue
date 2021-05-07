<template>
  <div id="nav">
    <nav class="navbar navbar-expand-lg navbar-dark">
      <a class="navbar-brand" href="/">Felix Bonillo</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav ml-auto">
          <li class="nav-item active">
            <a class="nav-link"> <router-link to="/">Home</router-link> </a>
          </li>
          <li class="nav-item">
            <a class="nav-link"><router-link to="/about">About</router-link></a>
          </li>
          <li class="nav-item">
            <a class="nav-link"><router-link to="/services">Services</router-link></a>
          </li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
              <router-link to="/pages">Pages</router-link>
            </a>
            <div class="dropdown-menu" aria-labelledby="navbarDropdown">
              <a class="dropdown-item" href="#">Action</a>
              <a class="dropdown-item" href="#">Another action</a>
            </div>
          </li>
          <li class="nav-item">
            <a class="nav-link"><router-link to="/contact">Contact</router-link></a>
          </li>
        </ul>
      </div>
    </nav>
  </div>
</template>

<script>

export default {
    name: 'NavBar',
    components: {
    }

}
</script>

<style scoped>
#nav {
  background-color: transparent;
  position: absolute;
  width: 100%;
  z-index: 1;
}


#nav .dropdown-menu{
  background: transparent;
  border: none;
}

#nav {
  padding: 20px;
}

#nav a {
  font-weight: bold;
  color: #ffffff;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

</style>
