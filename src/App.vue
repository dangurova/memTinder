<template>
  <div id="app">
    <FinishPage v-if="isLogin && isFinaled" />
    <MemesList v-if="isLogin && !isFinaled" :key="indexByMem" :index="indexByMem" @set:index="this.setIndexbyMem"/>
    <LoginPage v-else msg="Welcome to the memTinder" @set:login="this.setLogin"/>
  </div>
</template>

<script>
import LoginPage from './components/LoginPage.vue';
import MemesList from './components/MemesList.vue';
import FinishPage from './components/FinishPage.vue';

export default {
  name: 'App',
  components: {
    LoginPage,
    MemesList,
    FinishPage
  },
  data: function() {
    return {
      isLogin: false,
      indexByMem: 1,
      isFinaled: false,
    }
  },
  methods: {
    setLogin: function (login) {
      if (login) {
        this.isLogin = true;
        console.log(login);
      }
    },
    setIndexbyMem: function () {
      if (this.indexByMem <= 9) {
        this.indexByMem += 1;
      } else {
        this.isFinaled = true;
      }
    }
  }
}
</script>

<style>
h1 {
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;
  width: 100%;
  height: 100vh;
}
</style>
