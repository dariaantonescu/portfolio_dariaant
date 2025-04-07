<template>
    <section class="illustrations-section py-16 px-8">
      <h2 class="text-4xl font-bold text-gray-900 mb-10 text-left">Art & Play</h2>
      
      <!-- Images and Text Container -->
      <div class="illustrations-container grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- Image 1 -->
        <div class="illustration-image">
          <img src="/visuals/illustration1.jpg" alt="Illustration 1" class="w-full h-auto object-cover"/>
        </div>
        
        <!-- Image 2 -->
        <div class="illustration-image">
          <img src="/visuals/illustration2.jpg" alt="Illustration 2" class="w-full h-auto object-cover"/>
        </div>
        
        <!-- Image 3 -->
        <div class="illustration-image">
          <img src="/visuals/illustration3.jpg" alt="Illustration 3" class="w-full h-auto object-cover"/>
        </div>
        
        <!-- Image 4 -->
        <div class="illustration-image">
          <img src="/visuals/illustration4.jpg" alt="Illustration 4" class="w-full h-auto object-cover"/>
        </div>
  
        <!-- Image 5 (Horizontal) -->
        <div class="illustration-image col-span-2">
          <img src="/visuals/illustration5.jpg" alt="Illustration 5" class="w-full h-auto object-cover"/>
        </div>
  
        <!-- Image 6 (Vertical) -->
        <div class="illustration-image">
          <img src="/visuals/illustration7.jpg" alt="Illustration 7" class="w-full h-auto object-cover"/>
        </div>

        <!-- Image 7 (Horizontal) -->
        <div class="illustration-image col-span-2">
          <img src="/visuals/illustration6.jpg" alt="Illustration 6" class="w-full h-auto object-cover"/>
        </div>

        <!-- Image 8 (Vertical) -->
        <div class="illustration-image">
          <img src="/visuals/knock.jpg" alt="Illustration 8" class="w-full h-auto object-cover"/>
        </div>

        <!-- Image 9 (Horizontal) -->
        <div class="illustration-image col-span-2">
          <img src="/visuals/painting1.jpeg" alt="Illustration 9" class="w-full h-auto object-cover"/>
        </div>

        <!-- Image 10 (Vertical) -->
        <div class="illustration-image">
          <img src="/visuals/painting2.jpg" alt="Illustration 8" class="w-full h-auto object-cover"/>
        </div>

        <!-- Image 11 (Horizontal) -->
        <div class="illustration-image col-span-2">
          <img src="/visuals/art.jpg" alt="Illustration 11" class="w-full h-auto object-cover"/>
        </div>
      </div>
  
      <!-- Text below images -->
      <div class="text-container mt-8 text-center">
        <h3 class="text-2xl font-semibold text-gray-800">My name is Daria, and I’m here to break free from challenges!</h3>
        <p class="mt-4 text-lg text-gray-600 max-w-3xl mx-auto">
          I embrace the journey of creative problem-solving. I’m curious, explorative, and ready to tackle new ideas. Whether it’s through research, design, or art, I like to unwrap fresh solutions and push boundaries. I’m also creative, empathetic, fast, and always up for a good laugh — let’s break free and create something amazing together!
        </p>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: "IllustrationsSection"
  };
  </script>
  
  <style scoped>
  
  .illustrations-container {
    display: grid;
    grid-template-columns: repeat(1, 1fr); /* Default 1 column on small screens */
    gap: 24px; /* Spacing between images */
  }
  
  .illustration-image {
    width: 100%;
    height: auto;
  }
  
  .illustration-image img {
    width: 100%;
    height: auto;
    object-fit: cover;
  }
  
  .text-container {
    text-align: center;
  }
  
  .text-container h3 {
    font-size: 2rem;
    font-weight: bold;
    color: #333;
  }
  
  .text-container p {
    font-size: 1.125rem;
    color: #666;
    line-height: 1.5;
    margin-top: 1rem;
  }
  
  .text-container button {
    background-color: #1e3a8a;
    color: #fff;
    padding: 10px 20px;
    font-size: 1rem;
    border-radius: 25px;
    border: none;
    cursor: pointer;
  }
  
  .text-container button:hover {
    background-color: #0f266d;
  }
  
  /* Horizontal images should take up more space */
  .illustration-image.col-span-2 {
    grid-column: span 2;
  }
  
  /* Responsive design for grid */
  @media (min-width: 768px) {
    .illustrations-container {
      grid-template-columns: repeat(2, 1fr); /* 2 columns on medium screens */
    }
  }
  
  @media (min-width: 1024px) {
    .illustrations-container {
      grid-template-columns: repeat(3, 1fr); /* 3 columns on large screens */
    }
  }
  </style>
  