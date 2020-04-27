<template>
  <div id="app">
    <div class="main-wrapper">
      <task-bar></task-bar>
    <img id="fiber-icon" src="@/assets/logo.png" width="150px" alt="fiber-icon">
      <p class="fiber-title">Fiber</p>
      <p class="fiber-subtitle">Advanced software protector</p>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import HelloWorld from './components/HelloWorld.vue';
import TaskBar from "@/components/TaskBar.vue";

@Component({
  components: {
    TaskBar,
    HelloWorld,
  },
})
export default class App extends Vue {}
</script>

<style>
  /*normalize*/
  *{
    margin: 0;
    padding: 0;
  }
  html body{
    overflow: scroll;
    width: 100%;
    height: 100%;
  }
  body::-webkit-scrollbar{
    display: none;
  }
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 100%;
  height: 655px;
}
  .main-wrapper{
    width: 100%;
    height: 655px;
    background: linear-gradient(to bottom right, rgb(234, 81, 59), #f8af2a, #fdf13a);
    border-radius: 20px;
    transition: all 0.2s ease-in-out;
  }
  .main-wrapper:hover{
    transform: translate(0, -2px);
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
