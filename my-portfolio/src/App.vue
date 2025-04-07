<template>
  <div>
    <Hero />
    <section id="about" class="about-section py-16 text-center">
      <About />
    </section>

    <section id="projects" class="projects-section py-16 text-center">
      <Projects />
    </section>

    <section id="illustrations" class="illustrations-section py-16 text-center">
      <Art />
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact-section py-16 text-center">
      <Contact />
    </section>

    <!-- Footer Section -->
    <Footer />
  </div>
</template>

<script>
// Importing components
import Hero from  './components/Hero.vue';
import About from './components/About.vue';
import Projects from './components/Projects.vue';
import Art from './components/Art.vue';
import Contact from './components/Contact.vue';
import Footer from './components/Footer.vue';


export default {
  components: {
    Hero,
    About,
    Projects,
    Art, 
    Contact,
    Footer,
  },
};
</script>

<style scoped>
/* General layout styles */
body {
  font-family: Arial, sans-serif;
}

#about, #contact {
  padding: 4rem;
}

/* Smooth scrolling */
html {
  scroll-behavior: smooth;
}
</style>
