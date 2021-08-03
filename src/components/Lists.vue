<template>
  <ul>
    <Items v-for="todoObj in todos" :key="todoObj.id" :todo="todoObj"/>
  </ul>
</template>

<script>
import Items from "./Items";


export default {
  name: "Lists",
  components: {Items},
  data(){
    return {
      todos:[
        {id:'001',name:'eating',isok:false}
      ]
    }
  },
}
</script>

<style scoped>

</style>