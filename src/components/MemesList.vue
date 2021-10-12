<template>
  <div class="login">
    <h1 class="descriptions"> Сhoose your favorite memes! </h1>
    <img class="mem" src="../assets/memesList/1.jpeg" alt="mem" >
    <div class="icon-container">
        <i class="fas fa-times"></i>
        <i class="fas fa-check" size="lg"></i>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LoginPage',
  props: {
    msg: String
  }
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
.mem {
  width: auto;
  height: 320px;
  margin-top: 100px;
  margin-bottom: 50px;
  border-radius: 10px;
}
.icon-container {
    display: flex;
    justify-content: center;
}
.fa-check {
    margin-left:100px;
}
.fas {
    width: 20px;
}
.descriptions {
  padding-top: 30px;
}
@media(max-width: 425px){
.title, .descriptions {
  font-size: 26px;
}
}
</style>
