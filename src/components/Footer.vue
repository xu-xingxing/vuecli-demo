<template>
  <div id="footer">
    <p>{{ title }}@{{ copy_right }}</p>
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
      copy_right: '2020年vueDemo'
    }
  }
}
</script>

<style scoped>
 p {
   padding: 10px;
   text-align: center;
   color: rgb(0, 247, 255);
   background: #333;
 }
</style>