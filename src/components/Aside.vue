<template>
  <div >
    <p>HAPPY aside</p>
  </div>
</template>

<script lang="ts">
// import is from "electron-is";
// import { mapState } from "vuex";
//   import { ADD_TASK_TYPE } from '@shared/constants'
//   import LogoMini from '@/components/Logo/LogoMini'
import "@/components/Icons/menu-task";
import "@/components/Icons/menu-add";
import "@/components/Icons/menu-preference";
import "@/components/Icons/menu-about";

export default {
  name: "Aside",
  components: {},
  // computed: {
  //   ...mapState('app', {
  //     currentPage: state => state.currentPage
  //   }),
  //   asideDraggable: function () {
  //     return is.macOS()
  //   }
  // },
  methods: {
    //   showAddTask (taskType = ADD_TASK_TYPE.URI) {
    //     this.$store.dispatch('app/showAddTaskDialog', taskType)
    //   },
    //   showAboutPanel () {
    //     this.$store.dispatch('app/showAboutPanel')
    //   },
    //   nav (page) {
    //     this.$router.push({
    //       path: page
    //     }).catch(err => {
    //       console.log(err)
    //     })
    //   }
  }
};
</script>

<style lang="scss">
  .aside-inner {
    display: flex;
    height: 100%;
    flex-flow: column;
  }
  .logo-mini {
    margin-top: 40px;
  }
  .menu {
    list-style: none;
    padding: 0;
    margin: 0 auto;
    user-select: none;
    cursor: default;
    > li {
      width: 32px;
      height: 32px;
      margin-top: 24px;
      cursor: pointer;
      border-radius: 16px;
      transition: background-color 0.25s;
      &:hover {
        background-color: rgba(255, 255, 255, 0.15);
      }
    }
    svg {
      padding: 6px;
      color: #fff;
    }
  }
  .top-menu {
    flex: 1;
  }
  .bottom-menu {
    margin-bottom: 24px;
  }

</style>
