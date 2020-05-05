
<template>
  <div id="app">
    <div class="main-wrapper">
      <task-bar></task-bar>
      <transition mode="out-in">
        <router-view></router-view>
      </transition>
    </div>
  </div>
</template>


<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import HelloWorld from "./components/HelloWorld.vue";
import TaskBar from "./components/TaskBar.vue";
import Aside from "./components/Aside.vue";
import HomePageView from "@/components/HomePageView.vue";

@Component({
  components: {
    TaskBar,
	HelloWorld,
	// Aside,
	// HomePageView,
  }
})
export default class App extends Vue {

}
</script>

<style>
  .v-enter{
    opacity: 0;
  }
  .v-enter-active{
    transition: 0.2s;
  }
  .v-enter-to{
    opacity: 1;
  }
  .v-leave{
    opacity: 1;
  }
  .v-leave-to{
    opacity:0;
  }
  .v-leave-active{
    transition: 0.2s;
  }
  /*normalize*/
  *{
    margin: 0;
    padding: 0;
    user-select: none;
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

</style>
