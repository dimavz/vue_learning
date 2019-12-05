<template>
    <div id="app">
        <!--    <img alt="Vue logo" src="./assets/logo.png">-->
        <MyComponent msg="Welcome to Your Vue.js App"/>
        <Car :model="model" :year="year"></Car>
        <Car :model="model" :year="year"></Car>
    </div>
</template>

<script>
    import MyComponent from './components/MyComponent.vue'
    import Car from './components/Car.vue'

    export default {
        name: 'app',
        data() {
            return {
                model: 'Ford',
                year: 2017
            }
        },
        components: {
            MyComponent, Car
        }
    }
</script>

<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
