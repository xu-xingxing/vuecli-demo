<template>
  <div id="app">
    <h1>动态组件和keep-alive缓存</h1>
    <keep-alive>
       <component :is="form_component"></component>
    </keep-alive>
    <button @click=" form_component='form-one'">form-one</button>
    <button @click=" form_component='form-two'">form-two</button>
  </div>
</template>

<script>
import FormOne from './components/FormOne'
import FormTwo from './components/FormTwo'
export default {
  name: 'App',
  data() {
    return {
      form_component: 'form-two'
    }
  },
  components: {
    "form-one": FormOne,
    "form-two": FormTwo
  }
}
</script>

<style scoped>
  h2 {
    background: lightseagreen;
  }
</style>
