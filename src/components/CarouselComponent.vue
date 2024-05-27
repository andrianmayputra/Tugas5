<template>
    <div class="carousel">
      <div class="carousel-item" v-for="(image, index) in images" :key="index">
        <img :src="image" alt="Futsal Shoes">
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'CarouselComponent',
    data() {
      return {
        images: [
          'src/tokosepatu.jpeg',
          'https://via.placeholder.com/800x300?text=Slide+2',
          'https://via.placeholder.com/800x300?text=Slide+3',
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .carousel {
    display: flex;
    overflow: hidden;
    margin: 20px 0;
  }
  
  .carousel-item {
    min-width: 100%;
    transition: transform 0.5s ease;
  }
  
  .carousel-item img {
    width: 100%;
    height: auto;
  }
  </style>
  