<template>
    <div>
        <h1>Counter App</h1>
        <button @click="incrementCount">Clicked {{ count }} times</button>
    </div>
</template>

<script>
import CounterMix from "../mixins/counter"
    export default {
        name:'ClickCounter',
        mixins:[CounterMix]
    }
</script>

<style scoped>

</style>