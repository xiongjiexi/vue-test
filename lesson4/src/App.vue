<template>
  <div id="app">
    <el-tabs>
      <el-tab-pane name="Computed" label="计算属性">
        <Computed />
      </el-tab-pane>
      <el-tab-pane name="Watch" label="计算属性">
        <Computed />
      </el-tab-pane>
    </el-tabs>
    <router-view></router-view>
  </div>
</template>

<script>
import Computed from './components/Computed.vue'

export default {
  name: 'App',
  components: {
    Computed
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
