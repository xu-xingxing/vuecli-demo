<template>
  <div id="users">
    <h1>Users.vue</h1>
    <ul>
      <li v-for="(user, index) in users" :key="index">{{user}}</li>
    </ul>
    <p class="desc">
      在style标签中加入scoped之后，当前样式只针对当前组件起作用
      原理是给当前标签加上了一个唯一的属性值
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      users: ["小猪佩奇", "大象艾米莉", "小羊苏西"]
    }
  }
}
</script>

<style scoped>
  h1 {
    color: green;
  }
  .desc {
    color: red;
  }
</style>