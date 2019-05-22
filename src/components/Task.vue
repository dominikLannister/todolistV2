<template lang="html">
  <tr>
    <th>{{ id }}</th>
    <th>{{ actName }}</th>
    <th>{{ description }}</th>
    <button type="button" class="btn btn-success">Update</button>
    <button type="button" class="btn btn-danger" v-on:click="deleteTask">Delete</button>
  </tr>
</template>

<script>
import axios from 'axios';
const API = 'http://localhost:81/apiTodolist/delete.php';

export default {
  name: 'Task',

  props: {
    task: {
      Type: Object,
      required: true
    }
  },
  data() {
    return {
      id: this.task.id,
      actName: this.task.actName,
      description: this.task.description,
    }
  },
  methods: {
    deleteTask() {
      axios({
        method: 'post',
        url: `${API}`,
        data: {
          id: this.task.id
        }
      })
      .then(function(response){
        console.log(response);
      })
      .catch(function(error){
        console.log(error);
      })
    }
  }
}
</script>

<style lang="scss">
tr
{
  padding: 5px;

  button{
    margin: 4px;
    min-width: 85px;
  }
}
</style>
