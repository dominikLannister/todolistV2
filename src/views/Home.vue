<template>
<div class="home">
  <div class="main">
    <Navbar msg="Welcome to Your Vue.js App" />
    <div class="row">
      <Aside />
      <Main />
    </div>
    <ModalForm v-if="visible === true" />
    <Button @click.native="apiConncet" />
  </div>
  <Footer />
</div>
</template>

<script>
const API = 'http://localhost:81/apiTodolist/read.php';

import axios from 'axios';
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
    },
    apiConncet() {
      axios({
          method: 'get',
          url: 'http://localhost:81/apiTodolist/read.php',
          responseType: 'json'
        })
        .then((response) => {
          console.log(response);
        })
        .catch((error) => {
          console.log(error);
        });
    }
  }
}
</script>
<style lang="scss">

</style>
