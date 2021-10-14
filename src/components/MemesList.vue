<template>
  <div class="login">
    <h1 class="descriptions"> Сhoose your favorite memes! </h1>
    <img class="mem" :src="src" alt="mem" >
    <div class="icon-container">
        <i class="fas fa-4x fa-times" @click="$emit('set:index')"></i>
        <i class="fas fa-4x fa-check" @click="$emit('set:index')"></i>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LoginPage',
  data() {
    return {
    src: '',
    }
  },
  props: {
    msg: String,
    index: Number,
  },
    async created() {
    const fileModule = await import(`../assets/memesList/${this.index}.jpeg`);
    this.src = fileModule.default
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
@keyframes slide {
	0% {
        transform: translateX(100%) rotate(130deg);
	}
	70% {
        transform: translateX(30%) rotate(130deg);
	}
	100% {
        transform: translateX(0%) rotate(0deg);
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
  margin-top: 80px;
  margin-bottom: 50px;
  border-radius: 10px;
  /* animation: slide 1s 1; */
}
.icon-container {
    display: flex;
    justify-content: center;
}
.fa-check {
    margin-left:200px;
    width: 70px;
}
.fa-times {
    width: 70px;
    height: 64px;
}
.fas {
    animation: pulse 2s infinite;
    border-radius: 10px;
    background-color: rgba(255, 255, 255, 0.2);
    transition: background-color 1s linear;
    cursor: pointer;
}
.fas:active {
      -webkit-transform: scale(0.8);
  -ms-transform: scale(0.8);
  transform: scale(0.8);
}
.icon-container:hover .fas {
    animation: none;
}
.descriptions {
  padding-top: 50px;
}
@media(max-width: 425px){
.title, .descriptions {
  font-size: 26px;
}
}
</style>
