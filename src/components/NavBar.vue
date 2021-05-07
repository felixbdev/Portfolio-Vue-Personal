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
            <router-link class="link" to="/">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link class="link" to="/about">About</router-link>
          </li>
          <li class="nav-item">
            <router-link class="link" to="/services">Services</router-link>
          </li>
          <li class="nav-item">
            <router-link class="link" to="/contact">Contact</router-link>
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

.link{
  color: #fff;
  text-decoration: none;
  margin-right: 14px;
  font-weight: bold;

}


#nav a.router-link-exact-active {
  color: #42b983;
}

</style>
