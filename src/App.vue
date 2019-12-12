<template>
    <div id="app">
        <img alt="Vue logo" src="./assets/logo.png">
        <h1>Parent Model:{{model}}</h1>
        <MyComponent msg="Урок 37. Использование event emitter"/>
        <Counter></Counter>
        <Car :model="model" :year="year" @modelChange="model = $event" :changeFunc="changeModelToAudi"></Car>
        <Car :year="year" @counterUpdated="counter = $event"></Car>

    </div>
</template>

<script>
    import MyComponent from './components/MyComponent.vue'
    import Car from './components/Car.vue'
    import Counter from './components/Counter.vue'

    export default {
        name: 'app',
        data() {
            return {
                model: 'Ford',
                year: 2017,
            }
        },
        components: {
            MyComponent,
            Car,
            Counter,
        },
        methods:{
            changeModelToAudi(){
                this.model = 'Audi'
            }
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
