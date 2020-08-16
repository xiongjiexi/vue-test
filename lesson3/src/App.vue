<template>
  <div id="app">
    <input v-model="info">
    <button @click="addItem">add</button>
    <p>普通传值方式</p>
    <ul>
      <TodoList v-for="l in list" :key="l" :item="l"></TodoList>
    </ul>
    <br/>
    <p>插槽方式</p>
    <ul>
      <TodoList_slot v-for="x in list" :key="x">
        <span style="">{{x}}</span>
      </TodoList_slot>
    </ul>
    <br/>
    <p>checkbox变化颜色</p>
    <ul>
      <TodoList_checkbox v-for="x in list" :key="x">
        <template v-slot:item="itemProps">
          <span :style="{color : itemProps.checked ? 'red' : 'blue'}">{{x}}</span>
        </template>
      </TodoList_checkbox>
    </ul>
  </div>
</template>

<script>
import TodoList from './components/TodoList.vue'
import TodoList_slot from './components/TodoList_slot.vue'
import TodoList_checkbox from './components/TodoList_checkbox.vue'

export default {
  name: 'App',
  components: {
    TodoList,
    TodoList_slot,
    TodoList_checkbox
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
