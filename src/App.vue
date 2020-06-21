<template>
  <div id="app">
    <!-- <Header/> -->
    <!-- 传值 -->
    <Header :title="title" @ChageAppTitle="titleChange"></Header>
    <!-- 3.调用组件 -->
    <!-- 属性传值： 值有两种情况：1.传值（string, boolean, number) 2.传引用(object, array) -->
    <Users :users="users"/>
    <hr>
    <Users :users="users"/>
    <!-- <my-users></my-users> -->
    <!-- <p>子组件如果想使用父组件的样式，可以将scoped去掉</p> -->
    <Footer :title="title"/>
  </div>
</template>

<script>
// 1.引入组件
import Users from './components/Users'
import Header from './components/Header'
import Footer from './components/Footer'
export default {
  name: 'App',
  data() {
    return {
      users: [
        {name:   "小猪佩奇",age: 10, hobby: '吃饭',show: false},
        {name: "大象艾米莉",age: 10, hobby: '',show: false},
        {name:   "小羊苏西",age: 10, hobby: '吃饭睡觉打六六',show: false},
        {name:   "小猪佩奇",age: 10, hobby: '',show: false},
        {name: "大象艾米莉",age: 10, hobby: '睡觉打六六',show: false},
        {name:   "小羊苏西",age: 10, hobby: '',show: false},
        {name:   "小猪佩奇",age: 10, hobby: '吃饭',show: false}
      ],
      title: 'Hello mrokxu'
    }
  },
  components: {
    // 2.注册组件
    Users,
    // Users:Users
    // "my-users": Users
    Header,
    Footer
  },
  methods: {
    titleChange(val) {
      console.log(val)
      this.title = val
    }
  }
}
</script>

<style scoped>
h1 {
  color: purple;
}
</style>
