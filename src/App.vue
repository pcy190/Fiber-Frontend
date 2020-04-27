<template>
  <div id="app">
    <task-bar></task-bar>
    <div class="main-wrapper">
      <img alt="Vue logo" src="./assets/logo.png">
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
    height: 600px;
    background: linear-gradient(to bottom right, #0f2027, #203a43, #2c5364);
    border-radius: 20px;
    margin-top: 10px;
    transition: all 0.2s ease-in-out;
  }
  .main-wrapper:hover{
    transform: translate(0, -2px);
  }
</style>
