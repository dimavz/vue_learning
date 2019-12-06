<template>
    <div class="car">
        <h2>Model: {{model}} / {{reverseName}}</h2>
        <h2>Year: {{year}}</h2>
        <button @click="changeModel">Изменить модель</button>
        <button @click="changeFunc">Изменить модель из Родителя</button>
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
            },
            changeFunc:{
                type:Function
            }
        },
        computed:{
            reverseName(){
                return this.model.split('').reverse().join('')
            }
        },
        methods:{
            changeModel(){
                this.model = 'Mazda'
                this.$emit('modelChange', this.model +' '+ this.year)
                // Метод $emit передаёт событие (первый параметр) и значение (второй параметр) в родительский компонент
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
