<template>
  <div class="home">
    <div class="main">
      <Navbar msg="Welcome to Your Vue.js App"/>
      <div class="row">
        <Aside />
        <Main />
      </div>
      <div class="modalContainer">
        <ModalForm />
      </div>
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

 .main
 {
  position: relative;
  height: 100%;
 }
 .modalContainer
 {
   position: absolute;
   margin-left: auto;
   margin-right: auto;
   top: 50%;
   width: 100%;
   text-align: center;
 }

</style>
