<template>
  <div id="app">
    <!-- 方法一使用字符串形式将标签传给子组件 -->
    <!-- <FormHelper :title="title"/> -->
    <!-- 方法二使用slot插槽 -->
    <!-- 此种写法并不能将标签传给子组件 -->
    <!-- <FormHelper>
      <h2>这是个title</h2>
      <p>这个是文本内容</p>
    </FormHelper> -->
    <!-- <FormHelper>
      <h2>这是个title</h2>
      <p>这个是文本内容</p>
    </FormHelper> -->

    <!-- 给标签定义一个slot属性指定slot占的位置 -->
    <FormHelper>
      <h2 slot="h2">{{ title }}</h2>
      <p slot="p">给标签定义一个slot属性指定slot占的位置</p>
    </FormHelper>
  </div>
</template>

<script>
import FormHelper from './components/FormHelper'
export default {
  name: 'App',
  data() {
    return {
      // 起因：如果想给子组件传递标签怎么做？
      // 1.使用字符串形式
      title: "这是个title"
    }
  },
  components: {
    FormHelper
  },
  methods: {
  }
}
</script>

<style scoped>
  h2 {
    background: lightseagreen;
  }
</style>
