<template lang="html">
  <tr>
    <th>{{ id }}</th>
    <th>{{ actName }}</th>
    <th>{{ description }}</th>
    <button type="button" class="btn btn-success">Update</button>
    <button type="button" class="btn btn-danger">Warning</button>
  </tr>
</template>

<script>
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
