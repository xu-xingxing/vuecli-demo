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
  </div>
</template>

<script>
export default {
  data() {
    return {
      users: [
        {name:   "小猪佩奇",age: 10, hobby: '吃饭',show: false},
        {name: "大象艾米莉",age: 10, hobby: '',show: false},
        {name:   "小羊苏西",age: 10, hobby: '吃饭睡觉打六六',show: false},
        {name:   "小猪佩奇",age: 10, hobby: '',show: false},
        {name: "大象艾米莉",age: 10, hobby: '睡觉打六六',show: false},
        {name:   "小羊苏西",age: 10, hobby: '',show: false},
        {name:   "小猪佩奇",age: 10, hobby: '吃饭',show: false},
      ],
      is_show_hobby: false
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