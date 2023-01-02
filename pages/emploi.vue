<template>
    <div>
      <div>
          <div><Sidebar/></div>
          <div><Topbar/></div>
      </div>
    </div>
  </template>
  
  <script>
  import Sidebar from '../layouts/sidebar.vue';
  import Topbar from '../layouts/topbar.vue';
  export default {
      components: { Sidebar, Topbar }
  }
  </script>
  
  <style>
  
  </style>