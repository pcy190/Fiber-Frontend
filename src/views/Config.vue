<template>
    <div id="config">
        <div class="title">
            Choose Protection Params
        </div>
        <div class="conf-wrapper">
            <ul>
               <li class="param-wrapper">
                   <toggle-button :toggleid="getToggle1"></toggle-button>
               </li>
               <li class="param-wrapper">
                   <toggle-button :toggleid="getToggle2"></toggle-button>
               </li>
               <li class="param-wrapper">
                   <toggle-button :toggleid="getToggle3"></toggle-button>
               </li>
               <li class="param-wrapper">
                   <toggle-button :toggleid="getToggle4"></toggle-button>
               </li>
                <li class="param-wrapper">
                    <toggle-button :toggleid="getToggle5"></toggle-button>
                </li>
                <li class="param-wrapper">
                    <toggle-button :toggleid="getToggle6"></toggle-button>
                </li>
                <li class="param-wrapper">
                    <toggle-button :toggleid="getToggle7"></toggle-button>
                </li>
                <li class="param-wrapper">
                    <toggle-button :toggleid="getToggle8"></toggle-button>
                </li>
            </ul>
        </div>
        <ul class="button-wrapper">
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
    import ToggleButton from "../components/ToggleButton";
    export default {
        components: {ToggleButton},
        methods:{
          goHome: function () {
            this.$router.go(-1);
          }
        },
        data(){
            return {
                getToggle1: 'toggle1',
                getToggle2: 'toggle2',
                getToggle3: 'toggle3',
                getToggle4: 'toggle4',
                getToggle5: 'toggle5',
                getToggle6: 'toggle6',
                getToggle7: 'toggle7',
                getToggle8: 'toggle8',

            }
        },
        name: "Config"
    }
</script>

<style scoped>
    .conf-wrapper{
        display: block;
    }
    .conf-wrapper ul{
        position: relative;
        list-style: none;
        width: 600px;
    }
    .param-wrapper{
        width: 300px;
        display: inline-block;
    }
    .button-wrapper{
        list-style: none;
    }
    .button-wrapper li {
        display: inline-block;
        padding-left: 10px;
        padding-right: 10px;
    }
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
