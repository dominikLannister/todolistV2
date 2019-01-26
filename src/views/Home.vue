<template>
  <div class="home">
    <Navbar msg="Welcome to Your Vue.js App"/>
    <Aside />
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue'
import Aside from '@/components/Aside.vue'


export default {
  name: 'home',
  components: {
    Navbar,
    Aside
  }
}
</script>
<style lang="scss">

</style>
