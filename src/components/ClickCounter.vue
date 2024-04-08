<template>
    <div>
        <h1>Counter App</h1>
        <button @click="incrementCount" class="button"><span>Clicked<b class="bold"> {{ count }}</b> times</span></button>
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
.bold{
    color: teal;
}
 .button {
  display: inline-block;
  border-radius: 4px;
  background-color: #f4511e;
  border: none;
  color: #FFFFFF;
  text-align: center;
  font-size: 18px;
  padding: 20px;
  width: 200px;
  transition: all 0.5s;
  cursor: pointer;
  margin: 5px;
}

.button span {
  cursor: pointer;
  display: inline-block;
  position: relative;
  transition: 0.5s;
}

.button span:after {
  content: '\00bb';
  position: absolute;
  opacity: 0;
  top: 0;
  right: -20px;
  transition: 0.5s;
}

.button:hover span {
  padding-right: 25px;
}

.button:hover span:after {
  opacity: 1;
  right: 0;
}

</style>