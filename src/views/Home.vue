<template>
  <div class="home">
    <Navbar msg="Welcome to Your Vue.js App"/>
    <div class="row">
      <Aside />
      <Main />
    </div>  
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue'
import Aside from '@/components/Aside.vue'
import Main from '@/components/Main.vue'

export default {
  name: 'home',
  components: {
    Navbar,
    Aside,
    Main
  }
}
</script>
<style lang="scss">

</style>
