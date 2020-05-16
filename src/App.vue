<template>
  <div id="app">
    <HelloWorld>
    </HelloWorld>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'  //HElloWorldをインポート
export default {
  name: 'app',
  components: {
    HelloWorld
  },
}
</script>
<!-- CSS -->
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size: 20px;
  color: #black;
  background-color: Wheat;
  margin: 5px;
}
.hello{
  text-align: left;
}
table{
  margin-right: auto;
  margin-left: auto;
}
tr td{
  padding: 5px;
  border: 1px solid gray;
}
tr th{
  padding: 5px;
  border: 5px;
}
tr th.head{
  background-color: black;
  color: white;
}
textarea{
  font-size: 20px;
  background-color: Wheat;
}
</style>
