<template>
  <div id="app">
     <headeer/>
     <contentbar/>
  </div>
</template>

<script>
import headeer from "@/widgets/header"
import contentbar from "@/widgets/contentbar"
export default {
  name: 'app',
  components: {
    headeer,
    contentbar
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  color: #2c3e50;
}
</style>
<style scoped>
/deep/ #headeer{
  position:fixed;
background-color:black;
height:6rem;
width:100%;
text-align:center;
color:white;


}
#app{
  height:100vh;
  width:100vw;
  background-color:black;
}
</style>
