<template>
  <div class="home">
    <img id="fiber-icon" src="@/assets/logo.png" width="150px" alt="fiber-icon">
    <p class="fiber-title">Fiber</p>
    <p class="fiber-subtitle">Advanced software protector</p>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>
<style scoped>
  #fiber-icon{
    margin-top: 80px;
  }
  .fiber-title{
    font-size: 60px;
    font-family: "Microsoft YaHei UI Light",sans-serif;
    margin-top: 20px;
  }
  .fiber-subtitle{
    font-size: 30px;
    margin-top: 10px;
    font-family: "Microsoft YaHei UI Light",sans-serif;
  }
</style>
