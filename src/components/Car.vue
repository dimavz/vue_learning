<template>
    <div class="car">
        <h2>Model: {{model}} / {{reverseName}}</h2>
        <h2>Year: {{year}}</h2>
    </div>
</template>

<script>
    export default {
        name: "Car",
        // props:['model','year']
        // props:{
        //     model: String,
        //     year:Number
        // },
        props:{
            model: {
                type:String,
                required:false,
                default: 'Default Auto'
            },
            year:{
                type: Number
            }
        },
        computed:{
            reverseName(){
                return this.model.split('').reverse().join('')
            }
        }

    }
</script>

<style scoped>
.car{
    border: 1px solid green;
    padding: 5px;
}
</style>
