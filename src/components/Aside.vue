<template lang="html">
  <aside class="col-3">
    <div class="timetable">
      <ul class="list-group">
        <li class="list-group-item active">Today</li>
        <li class="list-group-item">Week</li>
        <li class="list-group-item">Month</li>
        <li class="list-group-item">Year</li>
      </ul>
    </div>
    <div class="calendar">
      <ul class="nav">
        <li class="nav-item">
          <a class="nav-link active" href="#">Active</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Link</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Link</a>
        </li>
        <li class="nav-item">
          <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Disabled</a>
        </li>
      </ul>
    </div>
  </aside>
</template>

<script>
export default {
  name: 'Aside'
}
</script>

<style lang="scss">

 aside
 {
   margin-top: 10px;
   color: black;
 }
 .calendar
 {
  margin-top: 25px;
 }
</style>
