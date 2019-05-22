<template>
<div class="home">
  <Header />
  <div class="main">
    <div class="row">
    </div>
    <ModalForm v-if="visible === true" @closeModal="visible = false" :rowId="result"/>

  </div>
  <table class="table table-sm table-dark">
    <thead>
      <tr class="header">
        <th scope="col">#</th>
        <th scope="col">Act</th>
        <th scope="col">Description</th>
        <th scope="col">Options</th>
      </tr>
    </thead>
    <tbody>
      <Task v-for="result in results" :task="result" :key="result.id" />
    </tbody>
  </table>
  <div class="butttonContainer">
    <Button @click.native="modalOpen" />
  </div>
  <Footer />
</div>
</template>

<script>
import axios from 'axios';
import Header from '@/components/Header.vue'
import Aside from '@/components/Aside.vue'
import Main from '@/components/Main.vue'
import Footer from '@/components/Footer.vue'
import ModalForm from '@/components/ModalForm.vue'
import Button from '@/components/Button.vue'
import Task from '@/components/Task.vue'

const API = 'http://localhost:81/apiTodolist/read.php';

export default {
  name: 'home',
  components: {
    Header,
    Aside,
    Main,
    Footer,
    ModalForm,
    Button,
    Task,
  },

  data() {
    return {
      visible: false,
      results: [],
    };
  },

  methods: {
    modalOpen() {
      this.visible = true;
    },
    apiConncet() {
      axios({
          method: 'get',
          url: `${API}`,
          responseType: 'json'
        })
        .then((response) => {
          console.log(response.data);
          this.results = response.data;
        })
        .catch((error) => {
          console.log(error);
        });
    }
  },
  beforeMount() {
    this.apiConncet()
  },
}
</script>
<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Lato:300,400,700');
.home {
    font-family: 'Lato', sans-serif;

    .butttonContainer {
      display: flex;
      align-items: center;
    }
    th{
      padding: 8px !important;
    }
}



</style>
