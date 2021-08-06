<template>
  <li>
    v-modle 双向绑定 不建议 因为props是不能修改的，但是这样写就把props改掉了， vue可监测到简单类型的修改，但是监测不到对象中属性的修改
    <br/>
    <label>
<!--      <input type="checkbox" :checked="todo.done" @change="handleCheck(todo.id)"/>-->

      <input type="checkbox" v-model="todo.done"/>
      <span>{{ todo.name }}</span>
    </label>
  </li>
</template>

<script>
export default {
  name: "Items",
  props:['todo'],
}
</script>

<style scoped>

</style>