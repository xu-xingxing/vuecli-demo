<template>
  <div id="header">
   <h1>{{ title }}</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "Vue Components Demo"
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