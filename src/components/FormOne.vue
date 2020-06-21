<template>
  <div id="form-one">
    <form-helper>
      <div slot="form-header">
        <h3>Form One - Contact Us</h3>
        <p>填写以下内容</p>
      </div>
      <div slot="form-fields">
        <input type="text" placeholder="name" required>
        <label>随便说点啥</label>
        <textarea></textarea>
      </div>
      <div slot="form-controls">
        <button v-on:click="handleSubmit">发送</button>
      </div>
    </form-helper>
  </div>
</template>

<script>
  import FormHelper from './FormHelper'
  export default {
    name: 'FormOne',
    data() {
      return {

      }
    },
    components:{
      "form-helper":FormHelper
    },
    methods: {
      handleSubmit() {
        
      }
    }
  }
</script>

<style scoped>

</style>