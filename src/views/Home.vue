<template>
  <div class="home">
    <Navbar msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue'

export default {
  name: 'home',
  components: {
    Navbar
  }
}
</script>
<style lang="scss">
body
{
  background-color: #191d21;
}
</style>
