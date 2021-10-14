<template>
  <div class="finish">
    <h1 class="descriptions"> Thanks a lot for rating our memes! </h1>
    <img class="mem" src="http://i.imgur.com/4WlfWmX.png" alt="mem" >
    <button class="button" @click="() => {}"> Show recommendations </button>
  </div>
</template>

<script>
export default {
  name: 'FinishPage',
}
</script>

<style scoped>
h1 {
  list-style-type: none;
  padding: 0;
}
.finish {
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
}
.descriptions {
    padding-top: 100px;
}
.button {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    margin: 20px auto;
    height: 40px;
    display: block;
    background-color: transparent;
    border-radius: 5px;
    border: none;
    color: white;
    font-size: 26px;
    font-weight: bold;
    animation: pulse 2s infinite;
    border-radius: 10px;
    background-color: rgba(255, 255, 255, 0.2);
    transition: background-color 1s linear;
    cursor: pointer;
}
.button:active {
    -webkit-transform: scale(0.8);
    -ms-transform: scale(0.8);
    transform: scale(0.8);
}
.button:hover {
    animation: none;
}
@media(max-width: 425px){
    .title, .descriptions {
        font-size: 26px;
    }
}
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
</style>
