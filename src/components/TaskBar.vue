<template>
    <div id="task-bar">
        <div id="app-title">
            Fiber
        </div>
    </div>
</template>

<script>
    export default {
        name: "TaskBar"
    }
</script>

<style scoped>
#task-bar{
    -webkit-app-region: drag;
    width: 100%;
    height: 40px;
    border-radius: 20px;
}


    #app-title{
        color: white;
        position: relative;
        float: left;
        font-family: "Microsoft YaHei UI Light", sans-serif;
        font-size: 20px;
        margin-left: 20px;
        margin-top: 5px;
        letter-spacing: 1px;
    }
</style>
