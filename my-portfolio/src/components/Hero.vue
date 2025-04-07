<template>
    <section class="hero-container relative w-full h-screen overflow-hidden">
      <!-- Full-Screen MP4 Video Background -->
      <video autoplay muted loop class="video-background w-full h-full object-cover absolute top-0 left-0 z-0">
        <source src="/visuals/Animewebbg.mp4" type="video/mp4">
      </video>
  
      <Menu />
    </section>
  </template>
  
  <script>
  // Import the Menu component
  import Menu from './Menu.vue';
  
  export default {
    components: {
      Menu
    }
  };
  </script>
  
  <style scoped>
  .hero-container {
    position: relative;
    width: 100%;
    height: 100vh; 
    overflow: hidden;
  }
  
  .video-background {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover; 
    z-index: 0;
  }
  
  .text-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 10;
  }
  
  h1 {
    font-size: 4rem;
    font-weight: bold;
  }
  
  p {
    font-size: 1.25rem;
  }
  
  /* Ensure the Menu is positioned above the video */
  .menu-container {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 20; /* Menu stays above the video */
  }
  </style>
  