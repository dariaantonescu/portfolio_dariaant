<template>
    <div class="contact-container  md:px-16 lg:px-24 py-16">
      <!-- Contact heading -->
      <div class="text-left mb-8">
        <h2 class="text-4xl font-bold text-gray-900">Contact</h2>
        <p class="text-lg text-gray-600 mt-4">
          Whether you want to brainstorm, collaborate, or just chat about bananas and other ideas...
          I’m all ears (and peels)!
        </p>
      </div>
  
      <!-- Contact form or layout -->
      <div class="flex flex-col md:flex-row items-start justify-between gap-8 text-left">
        
        <!-- Left: Form -->
        <div class="contact-info md:w-1/2">
          <h3 class="text-2xl font-semibold text-gray-800 mb-4">Get in touch!</h3>
          <p class="text-lg text-gray-600 mb-6">
            I would love to hear from you! Drop me a message if you have any project ideas, questions, or just want to connect.
          </p>
          
          <!-- Contact form -->
          <form class="space-y-4">
            <input type="text" placeholder="Your Name" class="w-full p-3 border border-gray-300 rounded-md"/>
            <input type="email" placeholder="Your Email" class="w-full p-3 border border-gray-300 rounded-md"/>
            <textarea placeholder="Your Message" class="w-full p-3 border border-gray-300 rounded-md" rows="4"></textarea>
            <button type="submit" class="w-full bg-blue-800 text-white py-3 rounded-md">Send Message</button>
          </form>
        </div>
  
        <!-- Right: banana img -->
        <div class="banana-image md:w-1/2 flex justify-center">
          <img src="/visuals/banana.png" alt="Banana" class="w-full md:w-4/4 max-w-md object-contain"/>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "Contact",
  };
  </script>
  
  <style scoped>
  .contact-container {
    background-color:  rgb(234, 192, 7);
   width: 100%;
    height: 100vh;
  }
  
  .contact-info h3 {
    color: #1e3a8a;
  }
  
  .contact-info form input,
  .contact-info form textarea {
    width: 100%;
    padding: 0.75rem;
    border: 1px solid #e5e7eb;
    border-radius: 8px;
  }
  
  .contact-info form button {
    background-color: #1e3a8a;
    color: white;
    border-radius: 8px;
    font-weight: bold;
  }
  
  .contact-info form button:hover {
    background-color: #374151;
  }
  
  .banana-image img {
    max-width: 100%;
    object-fit: contain;
  }
  
  /* Responsive Design */
  @media (max-width: 768px) {
    .contact-info {
      width: 100%;
    }
    .banana-image {
      display: none;
    }
  }
  </style>
  