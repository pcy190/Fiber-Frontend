<template>
    <div id="config">
        <div class="title">
            Choose Protection Params
        </div>
        <ul>
            <li>
                <div class="button" @click="goHome">
                    Back
                </div>
            </li>
            <li>
                <div class="button">
                    Continue
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        methods:{
          goHome: function () {
            this.$router.go(-1);
          }
        },
        name: "Config"
    }
</script>

<style scoped>
    .title{
        position: relative;
        font-family: "Microsoft YaHei UI Light",sans-serif;
        color: black;
        font-size: 36px;
        text-align: center;
        letter-spacing: -1px;
        margin-top: 30px;

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
#config{
    position: relative;
    color: white;
}
</style>
