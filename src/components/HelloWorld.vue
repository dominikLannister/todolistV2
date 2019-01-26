<template lang="html">
  <nav class="navbar navbar-dark bg-jumpers navbar-expand-xl bg-primary">
    <a class="navbar-brand " href="#">ToDoList.pl</a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#mainmenu" aria-controls="mainmenu" aria-expanded="false"    aria-label="Przełącznik nawigacji">
     <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="mainmenu">
      <form class="form-inline my-2 my-lg-0 mr-auto ml-auto">
       <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
       <button class="btn  my-2 my-sm-0" type="submit">Search</button>
     </form>
     <button type="button" class="btn btn-secondary mr-2"  v-on:click="showModal">Add</button>
     <button type="button" class="btn btn-dark">Settings</button>
   </div>
  </nav>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
