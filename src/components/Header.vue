<template lang="html">
  <p>
    ToDoList.<span id="span">pl</span>
  </p>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style lang="scss" scoped>
  p{
    color: black;
    padding: 30px 0px 30px 0px;
    font-size: 37px;
    font-weight: bold;

    #span{
      color: #007bff;
    }
  }
</style>
