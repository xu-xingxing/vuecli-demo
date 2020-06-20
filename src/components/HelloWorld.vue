<template>
<!-- HTML结构：只能有一个根标签 -->
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>hobby: {{ hobby }}</p>
    <p>{{ greeting() }}</p>
  </div>
</template>

<script>
// js 逻辑
export default {
  name: 'HelloWorld',
  data() {
    return {
      msg: '米斯特okxu',
      hobby: '吃饭睡觉打66'
    }
  },
  methods: {
    greeting() {
      return `大家好，我叫${this.msg},我的爱好是${this.hobby}`
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* css样式 */
</style>
