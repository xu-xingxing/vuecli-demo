<template>
  <div id="form-helper">
    <h1>vue slot</h1>
    <!-- 方法一使用字符串形式将标签传给子组件 -->
    <!-- 将父组件传过来的标签显示出来 -->
    <!-- <div v-html="title"></div> -->

    <!-- 方法二使用slot接收传给子组件的标签 -->
    <!-- <p>slot相当于一个占位符，不管传递多少标签都可以显示出来</p>
    <p>以下是slot插入的内容</p>
    <slot></slot> -->

    <!-- 方法二使用情况指定占位的地方 -->
    <slot name="h2"></slot>
    <p>slot相当于一个占位符，不管传递多少标签都可以显示出来</p>
    <p>以下是slot插入的内容</p>
    <slot name="p"></slot>
  </div>
</template>

<script>
  export default {
    name: 'form-helper',
    props: {
      title: {
        type: String
      }
    },
    data() {
      return {
        
      }
    }
    
  }
</script>

<style scoped>
  /* // 对于给插槽中的标签设定样式，在插入的地方设定或者在使用的顶设定都可以 */
  h2 {
    background: lightseagreen;
  }
  
</style>