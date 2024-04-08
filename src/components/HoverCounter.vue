<template>
    <div>
        <h2>Hover Counter</h2>
        <h2 @mouseover="incrementCount">Hover Here,The count will Increase {{  count }}</h2>
    </div>
</template>

<script>
import CounterMixin from "../mixins/counter"
    export default {
        name:'HoverCounter',
        mixins:[CounterMixin]
        
    }
</script>

<style scoped>

</style>