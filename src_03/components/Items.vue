<template>
  <li>
    <label>
      <input type="checkbox" :checked="todo.done" @change="handleCheck(todo.id)"/>
      <span>{{ todo.name }}</span>
    </label>
    <button @click="deleteTodoObjOnly(todo.id)">删除</button>
  </li>
</template>

<script>
export default {
  name: "Items",
  props:['todo','changeStatus','deleteTodoObj'],
  methods:{
    handleCheck(id){
      // console.log('@',id)
      this.changeStatus(id)
    },
    deleteTodoObjOnly(id){
      if(confirm('确定删除吗？')){
        this.deleteTodoObj(id)
      }
    },
  },
}
</script>

<style scoped>

li button{
  float: right;
  display: none;
  margin-top: 3px;
}

li:hover{
  background-color: #42b983;
}

li:hover button{
  display: block;
}
</style>