<template lang="html">
      <div class="modalForm">
        <div class="modalContainer">
          <form class="form-inline">
            <div class="form-group mb-2">
              <label for="staticEmail2" class="sr-only">Email</label>
              <input type="text" readonly class="form-control-plaintext" id="staticEmail2" value="email@example.com">
            </div>
            <div class="form-group mx-sm-3 mb-2">
              <label for="inputPassword2" class="sr-only">Password</label>
              <input type="password" class="form-control" id="inputPassword2" placeholder="Password">
            </div>
            <button type="submit" class="btn btn-primary mb-2">Confirm identity</button>
          </form>
        </div>
        <span class="close">&times;</span>
      </div>
</template>

<script>
export default {
  name: 'ModalForm'
}
</script>

<style scoped lang="scss">

.modalForm
{
  width: 100%;
  height: 100%;
  position: fixed;
  display: none;
  padding-top: 120px;
  left: 0;
  right: 0;
  overflow: auto;
  background-color: rgba(0,0,0,0.9);
}
.modalContainer
{
  margin: auto;
  display: block;
  width: 70%;
  -webkit-animation-name: zoom;
  -webkit-animation-duration: 0.6s;
  animation-name: zoom;
  animation-duration: 0.6s;
}
@-webkit-keyframes zoom
{
  from {-webkit-transform:scale(0)}
  to {-webkit-transform:scale(1)}
}
@keyframes zoom {
  from {transform:scale(0)}
  to {transform:scale(1)}
}
.close
{
  position: absolute;
  top: 15px;
  right: 35px;
  color: #f1f1f1;
  font-size: 40px;
  font-weight: bold;
  transition: 0.3s;
}
.close:hover,
.close:focus
{
  color: #bbb;
  text-decoration: none;
  cursor: pointer;
}
@media only screen and (max-width: 700px)
{
.modal-content
{
  width: 100%;
}
}
</style>
