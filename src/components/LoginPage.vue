<template>
  <div class="login">
    <img class="logo" src="http://i.imgur.com/4WlfWmX.png" alt="logo">
    <h1 class="title" > Welcome to Memes Tinder! </h1>
    <h1 class="descriptions"> Rate memes and find new friends! </h1>
    <input class="field-by-login" placeholder=" enter login from instagram..." v-model.trim="login"/>
    <button class="save-button" @click="$emit('set:login', login)"> Go </button>
  </div>
</template>

<script>
export default {
  name: 'LoginPage',
  data: function() {
    return {
      login: '',
    }
  },
}
</script>

<style scoped>
@keyframes pulse {
	0% {
		-moz-box-shadow: 0 0 0 0 rgba(255,255,255, 0.7);
		box-shadow: 0 0 0 0 rgba(255,255,255, 0.7);
    -webkit-box-shadow: 0 0 0 0 rgba(255,255,255, 0.7);
	}
	70% {
		-moz-box-shadow: 0 0 0 10px rgba(255,255,255, 0);
		box-shadow: 0 0 0 10px rgba(255,255,255, 0);
    -webkit-box-shadow: 0 0 0 10px rgba(255,255,255, 0);
	}
	100% {
		-moz-box-shadow: 0 0 0 0 rgba(255,255,255, 0);
		box-shadow: 0 0 0 0 rgba(255,255,255, 0);
    -webkit-box-shadow: 0 0 0 0 rgba(255,255,255, 0);
	}
}
h1 {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.login {
  width: 100%;
  height: 100%;
  background: #4C58C6;
  backdrop-filter: blur(50px);
    background:
        linear-gradient(#40e6f5, transparent),
        linear-gradient(to top left, #0707db, #5e0fd4),
        linear-gradient(to top right, #5e0fd4, transparent);
    background-blend-mode: screen;
}
.logo {
  width: auto;
  height: 120px;
  padding-top: 100px;
  padding-bottom: 30px;
}
.descriptions {
  padding-top: 30px;
}

.field-by-login {
  width: 300px;
  height: 25px;
  border-radius: 10px;
  border: none;
  margin-top: 40px;
  font-size: 14px;
  box-shadow: 0 1px 4px 0 rgb(255 255 255 / 44%);
  animation: pulse 2s infinite;
}
.save-button {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  margin: 20px auto;
  display: block;
  background-color: transparent;
  border-radius: 5px;
  border: none;
  color: white;
  font-size: 22px;
  font-weight: bold;
}
.save-button:hover {
  background-color: rgba(255, 255, 255, 0.2);
  cursor: pointer;
  animation: none;
}
@media(max-width: 425px){
.title, .descriptions {
  font-size: 26px;
}
}
</style>
