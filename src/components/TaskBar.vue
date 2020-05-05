<template>
    <div id="task-bar">
        <div id="app-title">
            Fiber
        </div>
        <div class="drag-zone"></div>
        <ul class="button-wrapper">
            <li class="button button-green"></li>
            <li class="button button-yellow" @click="minClick"></li>
            <li class="button button-red" @click="quitClick"></li>
        </ul>
    </div>
</template>

<script>
    const { ipcRenderer: ipc} = require('electron');
    export default {
        name: "TaskBar",
        methods: {
            minClick: function () {
                ipc.send('min');
            },
            quitClick: function () {
                ipc.send('quit');
            }
        }
    }
</script>

<style scoped>
#task-bar{
    width: 100%;
    height: 40px;
    border-radius: 20px;
    -webkit-app-region: drag;
}
.button-wrapper{
    float: right;
    list-style: none;
    margin-right: 5px;
    margin-top: 10px;
}
.button{
    width: 20px;
    height: 20px;
    border-radius: 100%;
    background: #42b983;
    display: inline-block;
    margin-right: 10px;
    -webkit-app-region: no-drag;
}
.button-green{
    background: #2ac83f;
    border: #2abf3e solid 0.2px;
    transition: all 0.2s ease-in-out;
}
.button-green:hover{
    background: #2fe247;
}
.button-yellow{
    background: #fdbd30;
    border: #f6b930 solid 0.2px;
    transition: all 0.2s ease-in-out;
}
.button-yellow:hover{
    background: #fddb30;
}
.button-red{
    background: #fd5f58;
    border: #e5564f solid 0.2px;
    transition: all 0.2s ease-in-out;
}
.button-red:hover{
    background: #fc473f;
}
    #app-title {
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
