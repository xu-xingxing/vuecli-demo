<template>
  <div id="header" @click="changeTitle">
   <h1>{{ title }}</h1>
   <p>传值只会影响自身</p>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String
    }
  },
  data() {
    return {
      // title: "Vue Components Demo"
    }
  },
  methods: {
    changeTitle() {
      // 本质上不能在子组件中修改父组件传过来的内容
      // this.title = "hello 米斯特okxu修改了title值"

      // 可以使用注册事件的方法
       this.$emit('ChageAppTitle', "hello 米斯特okxu通过$emit注册事件修改了title值")
    }
  }
}
</script>

<style scoped>
  #header {
    padding: 10px;
    background: rgb(0, 247, 255);
  }
  h1 {
    color: #333;
    text-align: center;
  }
</style>