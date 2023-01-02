<template>
  <div>
    <b-button size="is-large" icon-left="magnify" class="b-contact"
      >recherche</b-button
    >
  </div>
</template>

<script>
export default {};
</script>

<style>
.b-contact {
  background-color: #ffc30f;
  border: 0px;
  width: 180px;
  height: 50px;
  color: white;
  font-size: 20px;
  font-weight: 500;
  z-index: 100;
  position: fixed;
  border-radius: 30px;
  margin-left: 1160px;
  top: 90vh;
}
.b-contact:hover {
  color: white;
}
.magnify {
  padding-right: 10px;
  font-size: 28px;
}
</style>
