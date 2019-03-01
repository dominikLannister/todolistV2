<template lang="html">
      <div class="modalForm">
        <div class="modalContainer">
          <form class="form-inline">
            <div class="form-group mb-2">
              <label for="staticEmail2" class="sr-only">Task</label>
              <input type="text"  class="form-control" id="staticEmail2" placeholder="Task">
            </div>
            <div class="form-group mx-sm-3 mb-2">
              <label for="inputPassword2" class="sr-only">Description</label>
              <input type="password" class="form-control" id="inputPassword2" placeholder="Description">
            </div>
            <button type="submit" class="btn btn-primary mb-2">Add Task</button>
          </form>
        </div>
        <span class="close">&times;</span>
      </div>
</template>

<script>


export default {
  name: 'ModalForm',
}

</script>

<style scoped lang="scss">
.modalForm {
    width: 100%;
    height: 100%;
    position: fixed;
    display: block;
    z-index: 1;
    left: 0;
    top: 0;
    overflow: auto;
    background-color: rgba(0,0,0,0.9);
}
.modalContainer {
    padding: 50px;
    display: block;
    margin: 100px auto auto;
    width: 70%;
    -webkit-animation-name: zoom;
    -webkit-animation-duration: 0.6s;
    animation-name: zoom;
    animation-duration: 0.6s;
    background-color: white;
    border-radius: 1px;
}
form {
    width: 80%;
    margin: auto;
    padding: auto;
}
@-webkit-keyframes zoom {
    from {
        -webkit-transform: scale(0);
    }
    to {
        -webkit-transform: scale(1);
    }
}
@keyframes zoom {
    from {
        transform: scale(0);
    }
    to {
        transform: scale(1);
    }
}
.close {
    position: absolute;
    top: 15px;
    right: 35px;
    color: #f1f1f1;
    font-size: 40px;
    font-weight: bold;
    transition: 0.3s;
}
.close:focus,
.close:hover {
    color: #bbb;
    text-decoration: none;
    cursor: pointer;
}
@media only screen and (max-width: 700px) {
    .modal-content {
        width: 100%;
    }
}
</style>
