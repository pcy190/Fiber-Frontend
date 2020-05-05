<template>
  <div class="home">
	<!-- <button>HAPPY</button> -->
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script lang="ts">
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomePageView',
  components: {
    HelloWorld
  }
}
</script>
