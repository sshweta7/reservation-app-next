<template>
  <div id="app" class="container-fluid">
    <Customheader></Customheader> 
    <DeskDetail></DeskDetail>
    <Customfooter></Customfooter>
  </div>
</template>

<script>
import Customheader from './components/layout/Header';
import DeskDetail from './components/desk/DeskDetail';
import Customfooter from './components/layout/Footer';

export default {
  name: 'app',
  components: {
    Customheader, DeskDetail, Customfooter
  },  
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: #1979ba;
}

h1, h2 {
  font-weight: normal;
}

ul {
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
</style>
