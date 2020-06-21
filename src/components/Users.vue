<template>
  <div id="users">
    <ul>
      <li v-for="(user, index) in users" :key="index" @click="user.show = !user.show">
        <h2>name: {{ user.name }}</h2>
        <h3>age: {{ user.age }}</h3>
        <p v-show="user.show">hobby: {{ user.hobby }}</p>
      </li>
    </ul>
    <!-- <p class="desc">
      在style标签中加入scoped之后，当前样式只针对当前组件起作用
      原理是给当前标签加上了一个唯一的属性值
    </p> -->
    <!-- 传引用 -->
    <button @click="deleteUser">delete user</button>
    <p>传引用如果对引用进行一些操作的话，会影响到其他地方的引用</p>
  </div>
</template>

<script>
export default {
  // 写法一
  // props: ["users","user2", "users3"],
  // 写法二
  // 多个属性往后写就行了
  props: {
    users: {
      // 定义接收数据的类型
      type: Array,
      // require 表示的是必须要传的属性
      require: true
    },
    user1: {

    },
    user2: {

    }
  },
  data() {
    return {
      is_show_hobby: false
    }
  },
  methods: {
    deleteUser() {
      this.users.pop()
    }
  }
}
</script>

<style scoped>
  #users {
    width: 100%;
    max-width: 1200px;
    margin: 40px auto;
    padding: 0 20px;
    box-sizing: border-box;
  }
  h1 {
    color: green;
  }
  .desc {
    color: red;
  }
  ul {
    display:flex;
    flex-wrap: wrap;
    list-style-type: none;
    padding: 0;
  }
  li {
    flex-grow: 1;
    flex-basis: 200px;
    text-align: center;
    padding: 30px;
    border: 1px solid #ccc;
    margin: 10px;
  }
</style>