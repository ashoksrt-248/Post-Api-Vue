<template>
    <div>
        <h2>Hover Counter</h2>
        <h2 @mouseover="incrementCount">Hover Here,The count will Increase {{  count }}</h2>
    </div>
</template>

<script>
    export default {
        name:'HoverCounter',
        data(){
            return{
                count:0
            }
        },
        methods:{
            incrementCount(){
                this.count += 1
            }
        }
    }
</script>

<style scoped>

</style>