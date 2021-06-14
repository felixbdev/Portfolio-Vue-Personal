<template>
  <NavBar />
  <router-view v-slot="{ Component }">
    <transition name="fade" mode="out-in">
      <component :is="Component" />
    </transition>
  </router-view>
</template>

<script>
import NavBar from "./components/NavBar";

export default {
  name: "app",
  components: {
    NavBar
  }
};
</script>

<style>
#app {
  font-family: Overpass, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

/*Scroll */

::-webkit-scrollbar {
  width: 8px;
}
::-webkit-scrollbar-track {
  box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
  border-radius: 10px;
}
::-webkit-scrollbar-thumb {
  border-radius: 12px;
  background-color: #fca211d5;
}

/*Efecto */

.fadeTop {
  opacity: 0;
  transform: translate(0, 10vh);
  transition: all 1.3s;
}

.fadeRight {
  opacity: 0;
  transform: translate(10vh, 0vh);
  transition: all 1s;
}

.fadeLeft {
  opacity: 0;
  transform: translate(-10vh, 0vh);
  transition: all 1s;
}

.visible {
  opacity: 1;
  transform: translate(0, 0);
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
