<template>
<img alt="Vue logo" src="./assets/logo.png">
<HelloWorld msg="Welcome to  Titus's App" />
<LoginComp/>
<ConditionComp />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import LoginComp from './components/LoginComp.vue';
// import ConditionComp from './components/ConditionComp.vue';

export default {
    name: 'App',
    components: {
        HelloWorld,
       LoginComp,
       // ConditionComp,
    }
}
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
