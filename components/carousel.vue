<template>
    <div>
      <VueSlickCarousel v-bind="settings">
        <div><img src="../assets/biblio.jpg" alt="" width="400px"></div>
        <div><img src="../assets/biblio.jpg" alt="" width="400px"></div>
        <div><img src="../assets/biblio.jpg" alt="" width="400px"></div>
        <div><img src="../assets/biblio.jpg" alt="" width="400px"></div>
        <div><img src="../assets/biblio.jpg" alt="" width="400px"></div>
        <div><img src="../assets/biblio.jpg" alt="" width="400px"></div>
        <div><img src="../assets/biblio.jpg" alt="" width="400px"></div>
       
      </VueSlickCarousel>
    </div>
  </template>
  
  <script>
    import VueSlickCarousel from 'vue-slick-carousel'
    import 'vue-slick-carousel/dist/vue-slick-carousel.css'
    // optional style for arrows & dots
    import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
  
  export default {
      components: { VueSlickCarousel },
    data: function () {
      return {
       settings:{
        dots: true,
        focusOnSelect: true,
        infinite: true,
        speed: 500,
        slidesToShow: 3,
        slidesToScroll: 3,
        touchThreshold: 5,
        autoplay: true,
    autoplaySpeed: 2000,
       }
      };
    },
  };
  </script>
  
  <style></style>
  