<template>
    <div >
      <div>
        <b-button to="/" class="b-button" @click="contact()">
          <i class="mdi mdi-whatsapp"></i>Contactez-nous
        </b-button>
      </div>
      
    </div>
  </template>
  
  <script>
  export default {};
  </script>
  
  <style>
  .b-button {
    background-color: rgb(238, 62, 56);
    border: 0px;
    width: 210px;
    height: 50px;
    color: white;
    font-size: 20px;
    font-weight: 500;
    z-index: 999;
    position: fixed;
    padding-top: 3px;
    border-radius: 30px;
    margin-left: 3px;
    top: 90vh;
  }
  .b-button:hover {
    color: white;
  }
  .mdi-whatsapp {
    font-size: 28px;
    padding-right: 5px;
  }
  </style>
  