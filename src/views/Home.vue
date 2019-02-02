<template>
  <div class="home">
    <div class="main">
      <Navbar msg="Welcome to Your Vue.js App"/>
      <div class="row">
        <Aside />
        <Main />
      </div>
      <ModalForm />
    </div>
    <Footer />
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue'
import Aside from '@/components/Aside.vue'
import Main from '@/components/Main.vue'
import Footer from '@/components/Footer.vue'
import ModalForm from '@/components/ModalForm.vue'



export default {
  name: 'home',
  components: {
    Navbar,
    Aside,
    Main,
    Footer,
    ModalForm
  }
}
</script>
<style lang="scss">



</style>
