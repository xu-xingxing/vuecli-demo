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
  },
  //　生命周期函数
  beforeCreate() {
    alert('这个时候是实例还没有被创建，所以你无法知道data,也不能用watch监听')
  },
  created() {
    alert('这个时候实例已经被创建，可以得到data，调用watch监听，但是页面还是为空白的')
  },
  beforeMount() {
    alert('页面挂载前，此时页面依然是空白的，这时render函数被首次调用')
  },
  created() {
    alert('页面已经挂载了，这时你可以看到页面的内容，也可以访问到dom')
  },
  beforeUpdate() {
    alert('数据更新前，也就是虚拟DOM打补丁之前')
  },
  updated() {
    alert('数据已经更新完毕')
  },
  beforeDestroy() {
    alert('页面离开之前被调用，清除定时器，或者三方的一些DOM结构')
  },
  destroyed() {
    alert('实例已经完全被销毁')
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