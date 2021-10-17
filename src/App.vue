<template>
  <div id="app">
    <Navbar/>
    <router-view/>
  </div>
</template>
<script>
import Navbar from "@/components/navbar.vue"
export default {
  components:{
Navbar,
  }
}
</script>
<style lang="scss">
$theme-colors: (
  "purple":rgba(150, 107, 218, 1)

);

*{
  padding:0;
  margin:0;
  box-sizing: border-box;
}
 #app{
  padding:40px 40px;
}

@media (min-width:768px){
  #app{
  padding:70px 114px;
}
}

</style>