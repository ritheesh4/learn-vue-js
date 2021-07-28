<template>
  <div id="app">
    <HomeScreen msg="This is my first vue js app" />
    <Counter />
  </div>
</template>

<script>
import HomeScreen from "./components/HomeScreen.vue";
import Counter from "./components/Counter.vue";
import Vue from "vue";
import Vuex from "vuex";

Vue.use(Vuex);

const store = new Vuex.Store({
  state: {
    count: 0,
  },
  mutations: {
    increment(state) {
      state.count++;
    },
  },
  
});

store.commit("increment");

export default {
  name: "App",
  components: {
    HomeScreen,
    Counter,
  },
};

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
