<template>
    <div>
      <div class="tap-bar box is-flex is-flex-direction-row is-justify-content-space-between">
          <div class="pl-20"><p class="tb"><nuxt-link to="/admin" class="t">Tableau de bord</nuxt-link></p></div>
          <div></div>
          <div class="is-flex deconnexion">
              <div class="pr-5"><i class="mdi mdi-account"></i>admin</div>
              <div class="pr-1"><i class="mdi mdi-logout"></i>Se deconnecter</div>
          </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
  
  }
  </script>
  
  <style>
  .top-bar{
      width: 100%;
      height: 40px;
      border-radius: 0px;
  }
  .pl-20{
      padding-left: 200px;
  }
  .tb > .t{
    color: black;
    padding-left: 10px;
  }

  
  </style>