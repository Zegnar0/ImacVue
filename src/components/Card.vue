<template>
    <div class="card">
      <img :src="imageUrl" alt="Card Image" class="card-image">
      <div class="card-content">
        <h3 class="card-title">{{ title }}</h3>
        <p class="card-description">{{ description }}</p>
        <button @click="handleButtonClick" class="card-button">Click me</button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      imageUrl: {
        type: String,
        required: true
      },
      title: {
        type: String,
        required: true
      },
      description: {
        type: String,
        required: true
      }
    },
    methods: {
      handleButtonClick() {
        alert('Button clicked!');
      }
    }
  };
  </script>
  
  <style scoped>
  .card {
    width: 300px;
    border: 1px solid #ccc;
    border-radius: 8px;
    overflow: hidden;
    margin: 16px;
  }
  
  .card-image {
    width: 100%;
    height: 150px;
    object-fit: cover;
  }
  
  .card-content {
    padding: 16px;
  }
  
  .card-title {
    font-size: 1.2em;
    margin-bottom: 8px;
  }
  
  .card-description {
    color: #555;
    margin-bottom: 16px;
  }
  
  .card-button {
    padding: 8px 16px;
    background-color: #007bff;
    color: #fff;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    outline: none;
  }
  
  /* Responsive Styling */
  @media (max-width: 768px) {
    .card {
      width: 100%;
    }
  }
  </style>
  