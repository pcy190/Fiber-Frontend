<template>
    <div class="toggles">
        <input type="checkbox" name="togglebtn" class="togglebtn" :id="toggleid">
        <label :for="toggleid"></label>
    </div>
</template>

<script>
    export default {
        name: "ToggleButton",
        props: {
            toggleid:{
                type: String,
                default: "toggle1"
            }
        }
    }
</script>

<style scoped>
    .toggles{
        position: relative;
        display: inline-block;
    }
    .toggles input.togglebtn {
        opacity: 0;
        position: relative;
    }
    .toggles input.togglebtn + label {
        position: relative;
        display: inline-block;
        -webkit-user-select: none;
        -moz-user-select: none;
        -ms-user-select: none;
        user-select: none;
        -webkit-transition: 0.4s ease;
        transition: 0.4s ease;
        height: 30px;
        width: 50px;
        border: 1px solid #e4e4e4;
        border-radius: 60px;
    }
    .toggles input.togglebtn + label:before {
        content: "";
        position: absolute;
        display: block;
        -webkit-transition: 0.2s cubic-bezier(0.24, 0, 0.5, 1);
        transition: 0.2s cubic-bezier(0.24, 0, 0.5, 1);
        height: 30px;
        width: 51px;
        top: 0;
        left: 0;
        border-radius: 30px;
    }
    .toggles input.togglebtn + label:after {
        content: "";
        position: absolute;
        display: block;
        box-shadow: 0 0 0 1px hsla(0, 0%, 0%, 0.1), 0 4px 0px 0 hsla(0, 0%, 0%, 0.04), 0 4px 9px hsla(0, 0%, 0%, 0.13), 0 3px 3px hsla(0, 0%, 0%, 0.05);
        -webkit-transition: 0.35s cubic-bezier(0.54, 1.6, 0.5, 1);
        transition: 0.35s cubic-bezier(0.54, 1.6, 0.5, 1);
        background: whitesmoke;
        height: 28px;
        width: 28px;
        top: 1px;
        left: 0px;
        border-radius: 60px;
    }
    .toggles input.togglebtn:checked + label:before {
        background: #2ecc71;
        -webkit-transition: width 0.2s cubic-bezier(0, 0, 0, 0.1);
        transition: width 0.2s cubic-bezier(0, 0, 0, 0.1);
    }
    .toggles input.togglebtn:checked + label:after {
        left: 24px;
    }
</style>
