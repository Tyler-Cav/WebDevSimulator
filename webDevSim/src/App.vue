<script setup>
import {ref, computed} from 'vue'
import HelloWorld from './components/HelloWorld.vue'
import Test from './components/test.vue'
import Welcome from './components/audio.vue'
const routes = {
  '/': HelloWorld,
  '/test': Test
}

const currentPath = ref(window.location.hash)

window.addEventListener('hashchange', () => {
  currentPath.value = window.location.hash
})

const currentView = computed(() => {
  return routes[currentPath.value.slice(1) || '/'] || NotFound
})
</script>

<template>
  <nav>
    <a href="/" class="idk">Home</a>
    <a href="#/test">Test</a>
    <component :is="currentView" />
  </nav>
  <Welcome/>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  
</template>


<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
.idk{
  margin: 10px;
}
</style>
