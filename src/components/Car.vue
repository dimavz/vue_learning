<template>
    <div class="car">
        <h2>Model: {{model}}</h2>
        <h2>Year: {{year}}</h2>
    </div>
</template>

<script>
    export default {
        name: "Car",
        props:{
            model: String,
            year:Number
        }
        // props:['model','year']
    }
</script>

<style scoped>
.car{
    border: 1px solid green;
    padding: 5px;
}
</style>
