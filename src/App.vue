<template>
  <div id="app">
    <!-- 3.调用组件 -->
    <Users/>
    <!-- <my-users></my-users> -->
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

<style>
</style>
