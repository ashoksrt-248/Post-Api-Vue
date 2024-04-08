<template>
  <div id="app">
    <h1>Post Api Call in VueJs</h1>
    <PostApi />
    <br />
    <br />
    <hr>
    <TemplateRef />
    <hr>
    <HoverCounter />
    <hr>
    <ClickCounter />
  </div>
</template>

<script>
import PostApi from './components/PostApi.vue';
import TemplateRef from './components/TemplateRef.vue';
import HoverCounter from './components/HoverCounter.vue';
import ClickCounter from './components/ClickCounter.vue';

export default {
  name: 'App',
  components: {
    PostApi,
    TemplateRef,
    HoverCounter,
    ClickCounter
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
