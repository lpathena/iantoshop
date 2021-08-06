<template>
 <div v-show="total">
   <label>
<!--     <input type="checkbox" :checked="isAll" @change="checkAll"/>  法1-->
     <input type="checkbox" v-model="isAll"/>
   </label>
   <span>
     <span>已经完成{{ doneTotal }}</span> / 全部{{ total }}
   </span>
   <button @click="clearCompletedItems">清除已完成任务</button>
 </div>
</template>

<script>
export default {
  name: "MyFooter",
  props:['todos','selectAllOrNot','deleteAllCompletedItems'],
  computed:{
    //法1
    // isAll(){
    //   return this.doneTotal === this.total && this.total > 0
    // },
    isAll:{
      get(){
        return this.doneTotal === this.total && this.total > 0
      },
      set(value){
        this.selectAllOrNot(value)
      }
    },
    total(){
      return this.todos.length
    },
    doneTotal(){
      // this.todos.reduce((pre,current)=>{
      //   return pre + (current.done ? 1 : 0)
      // },0)
      return this.todos.reduce((pre,todo)=> pre + (todo.done ? 1 : 0),0)
    }
  },
  //法1
  // methods:{
  //   checkAll(e){
  //     this.selectAllOrNot(e.target.checked)
  //   }
  // }
  methods:{
    clearCompletedItems(){
      this.deleteAllCompletedItems()
    }
  }
}
</script>

<style scoped>

</style>