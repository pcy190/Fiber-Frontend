<template>
  <div class="home">
    <img id="fiber-icon" src="@/assets/logo.png" width="150px" alt="fiber-icon">
    <p class="fiber-title">Fiber</p>
    <p class="fiber-subtitle">Advanced software protector</p>
    <ul class="button-wrapper">
      <li>
        <div class="button" @click="goConfig">
          Start Protect
        </div>
      </li>
      <li>
        <div class="button" @click="goAbout">
          About Fiber
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  methods: {
    goConfig: function () {
      this.$router.push('config')
    },
    goAbout: function () {
      this.$router.push('about')
    }
  },
  components: {
    HelloWorld
  }
}
</script>
<style scoped>
  .button-wrapper{
    list-style: none;
  }
  .button-wrapper li{
    display: inline-block;
    padding-left: 10px;
    padding-right: 10px;
  }
  .button{
    position: relative;
    width: 200px;
    height: 60px;
    background: #f44b2d;
    margin: 0 auto;
    margin-top: 60px;
    border-radius: 30px;
    box-shadow: 2px 2px 5px #621e0e;
    color: white;
    font-family: "Microsoft YaHei UI Light",sans-serif;
    letter-spacing: 0.5px;
    text-align: center;
    line-height: 60px;
    overflow: hidden;
    transition: all 0.2s ease-in-out;
  }
  .button:hover{
    background: #2abf3e;
    box-shadow: 2px 2px 5px #466d41;
  }
  .button:active{
    background: greenyellow;
    box-shadow: 2px 2px 5px #859113;
  }
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
