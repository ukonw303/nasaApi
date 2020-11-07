<template>
  <div id="app">
    <img class="img-circle" src="https://f.ptcdn.info/065/069/000/q92a41vcc9oFh7k4LvB-o.jpg" width="300px" height="150px">
    <br><Picture />
  </div>
</template>

<script>
import Picture from './components/pic'
export default {
  name: 'app',
  components: {
    Picture
  }
}
</script>

<style>
#app {
  font-family: 'Titillium Web', sans-serif;
  font-size: 18px;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #90caf9;
  margin-top: 60px;
}
.display-2{
  font-family: 'Baloo Tammudu 2', cursive;
  font-size: 40px;
  color: #afafaf;
}

body {
  background-image: url(https://d1csarkz8obe9u.cloudfront.net/posterpreviews/galaxy-background-design-template-e3a821c519b9d90c66c0b3a7b98cc874_screen.jpg?ts=1589084799);
  background-size:  100%;
}
</style>