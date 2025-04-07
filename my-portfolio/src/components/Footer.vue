<template>
    <footer class="footer mt-16 text-center p-8">
      <!-- Horizontal line -->
      <hr class="border-t-2 border-blue-800 mb-8" />
  
      <!-- Button Links: Projects, About, Contact aligned to the left -->
      <div class="flex justify-start gap-8">
        <a href="#projects" class="text-blue-800 font-semibold">Projects</a>
        <a href="#about" class="text-blue-800 font-semibold">About</a>
        <a href="#contact" class="text-blue-800 font-semibold">Contact</a>
      </div>
  
      <div class="mt-8 flex justify-end gap-8">
  <a href="https://www.instagram.com/dariaantonescu" target="_blank" class="text-blue-800 font-semibold">Instagram</a>
  <a href="https://www.linkedin.com/in/daria-antonescu" target="_blank" class="text-blue-800 font-semibold">LinkedIn</a>
</div>

  
      <p class="mt-8 text-lg text-gray-600">Let’s unpeel new ideas!</p>
    </footer>
  </template>
  
  <script>
  export default {
    name: "Footer",
  };
  </script>
  
  <style scoped>
  /* Styling for the Footer */
  footer {
    padding: 3rem 2rem;
  }
  footer hr {
    border-color: #1e3a8a;
  }
  footer .text-blue-800 {
    color: #1e3a8a;
  }
  footer .font-semibold {
    font-weight: 600;
  }
  </style>
  