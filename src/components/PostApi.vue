<template>
  <div>
    <form @submit.prevent="createPost">
      <div>
        <label for="userId">UserID</label>
        <input type="text" id="userId" v-model="FormData.userId"/>
      </div>
      <div>
        <label for="title">Title</label>
        <input type="text" id="title" v-model="FormData.title"/>
      </div>
      <div>
        <label for="body">Body</label>
        <input type="text" id="body" v-model="FormData.body"/>
      </div>
      <button>Create Post</button>
    </form>

  </div>
</template>

<script>
import axios from "axios"
  export default {
    name:'PostApi',
    data(){
      return{
        FormData:{
          userId:'',
          title:'',
          body:''
        }
      }
    },
    methods:{
      createPost(){
        axios.post('https://jsonplaceholder.typicode.com/posts', this.FormData)
        .then((response) => console.log(response))
      }
    }
  }
</script>

<style scoped>
  input[type=text] {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  box-sizing: border-box;
  border: 2px solid orange;
  border-radius: 3px;
  background-color: #3CBC8D;
  color: white;
}

</style>