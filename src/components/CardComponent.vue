<template>
    <div class="card">
      <img :src="image" alt="Product Image" class="card-img">
      <div class="card-body">
        <h3 class="card-title">{{ title }}</h3>
        <p class="card-price">{{ price }}</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'CardComponent',
    props: {
      image: String,
      title: String,
      price: String,
    },
  };
  </script>
  
  <style scoped>
  .card {
    border: 1px solid #ddd;
    border-radius: 5px;
    overflow: hidden;
    text-align: center;
    margin: 10px;
    width: 200px;
  }
  
  .card-img {
    width: 100%;
    height: 150px;
    object-fit: cover;
  }
  
  .card-body {
    padding: 10px;
  }
  
  .card-title {
    font-size: 18px;
    margin: 10px 0;
  }
  
  .card-price {
    font-size: 16px;
    color: #4CAF50;
    font-weight: bold;
  }
  </style>
  