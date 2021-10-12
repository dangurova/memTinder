<template>
  <div id="app">
    <MemesList v-if="isLogin" />
    <LoginPage v-else msg="Welcome to the memTinder" @set:login="this.setLogin"/>
  </div>
</template>

<script>
import LoginPage from './components/LoginPage.vue';
import MemesList from './components/MemesList.vue';

export default {
  name: 'App',
  components: {
    LoginPage,
    MemesList
  },
  data: function() {
    return {
      isLogin: true
    }
  },
  methods: {
    setLogin: function (login) {
      if (login) {
        this.isLogin = true;
        console.log(login);
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
