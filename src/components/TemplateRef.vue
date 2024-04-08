<template>
    <div>
        <h1>Template Ref Component</h1>
        <input type="text"  ref="inputRef"/>
    </div>
</template>

<script>
    export default {
        name:'TemplateRef',
        mounted(){
            this.$refs.inputRef.focus()
        }
    }
</script>

<style scoped>
    input:focus {
  background-color: yellow;
  width: 170px;
  height: 30px;
  color: brown;
}
</style>