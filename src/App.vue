<template>
  <div id="app">
    <h1>App.vue</h1>
    <!-- 3.调用组件 -->
    <Users/>
    <!-- <my-users></my-users> -->
    <p>子组件如果想使用父组件的样式，可以将scoped去掉</p>
  </div>
</template>

<script>
// 1.引入组件
import Users from './components/Users'
export default {
  name: 'App',
  components: {
    // 2.注册组件
    Users
    // Users:Users
    // "my-users": Users
  }
}
</script>

<style scoped>
h1 {
  color: purple;
}
</style>
