<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <input v-model="info">
    <button @click="addItem">add</button>
    <ul>
      <TodoList v-for="item in list" :key="item" :item="item"></TodoList>
    </ul>
  </div>
</template>

<script>
import TodoList from './components/TodoList.vue'

export default {
  name: 'App',
  components: {
    TodoList
  },
    data() {
        return {
            msg : "this is vue index",
            info : "",
            list : [],
        }
    },
    methods: {
        addItem() {
            this.list.push(this.info)
            this.info = ""
        }
    }
}
</script>

<style>

</style>
