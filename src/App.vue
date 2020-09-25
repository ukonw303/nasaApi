<template>
  <div id="app">
    <img class="img-circle" src="https://i.pinimg.com/originals/9c/b2/86/9cb2863a009b49fcc03161032e9e5baf.png" width="150px" height="150px">
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
  color: #e1bee7;
}

body {
  background-image: url(https://i2.wp.com/windowscustomization.com/wp-content/uploads/2019/07/Skyrim-NIght-Stars.gif?fit=768%2C432&quality=80&strip=all&ssl=1);
}
</style>