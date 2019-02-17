<template>
<div class="home">
  <div class="main">
    <Navbar msg="Welcome to Your Vue.js App" />
    <div class="row">
      <Aside />
      <Main />
    </div>
    <ModalForm v-if="visible === true" />
    <Button @click.native="modalOpen" />
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
import Button from '@/components/Button.vue'

export default {
  name: 'home',
  components: {
    Navbar,
    Aside,
    Main,
    Footer,
    ModalForm,
    Button,
  },

  data() {
    return {
      visible: false,
    };
  },

  methods: {
    modalOpen() {
      this.visible = true;
    }
  }
}
</script>
<style lang="scss">

</style>
