<template>
    <h1>Counter: {{counter}}</h1>
</template>

<script>
    export default {
        name: "Counter",
        props:{
            counter: {
                type:Number,
                required:false,
                default: 0
            }
        },
    }
</script>

<style scoped>

</style>
