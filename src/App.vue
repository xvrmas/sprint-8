<template>
  <div id="app">
    <!-- <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav>
    <router-view/> -->
    <home></home>
  </div>
</template>
<script>
import Home from './views/Home.vue'
export default {
  name: 'app',
  components: {
    Home
  }
}
</script>
<style>

</style>
